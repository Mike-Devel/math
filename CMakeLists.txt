# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(BoostMath)

add_library(boost_math INTERFACE)
add_library(Boost::math ALIAS boost_math)

target_include_directories(boost_math INTERFACE include)

target_link_libraries(boost_math
    INTERFACE
        Boost::array
        Boost::assert
        Boost::atomic
        Boost::concept_check
        Boost::config
        Boost::core
        Boost::detail
        Boost::fusion
        Boost::integer
        Boost::lambda
        Boost::lexical_cast
        Boost::mpl
        Boost::predef
        Boost::range
        Boost::smart_ptr
        Boost::static_assert
        Boost::throw_exception
        Boost::tuple
        Boost::type_traits
)

