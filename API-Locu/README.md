**Abstract**

This report outlines the Locu API, which allows for retrieval of menu information using spatial parameters. This data has potential to be used for mapping and analyzing accessibility to healthy foods. 

**What is Locu?**

Locu is a service that allows business to monitor and enhance their Internet visibility. It allows businesses to publish and update information regarding hours, menu items, and specials. 

**What is the Locu API?**

The Locu API allows registered users to search and access information about businesses and menus. 

**Does the API require a key?**

Yes, go here: [https://dev.locu.com/login/?next=/dashboard/](https://dev.locu.com/login/?next=/dashboard/)

**How do you find information for specific geographic areas?**

The [Venue Search API](https://dev.locu.com/documentation/) allows you to specify a geographic area using different parameters:

- Latitude, longitude, and radius (circular region)
- Latitude and longitude for top-left and bottom-right (bounding box)
- Administrative area: 
  - Country (eg, "United States")
  - Locality/city name (eg, "San Francisco")
  - Region/state/province (eg, "CA")
  - Postal code

**What information is available with respect to menus?**

The main information available is different menu sections, the price of each item, the name of each item, and a description of each item (though the description is frequently omitted). The information about specific attributes returned by in the JSON are documented [here](https://dev.locu.com/documentation/#menu). The following is an example of a menu for Bronx Pizza in San Diego:

Pizza by the Slice‏

    Cheese , 2.00 , [no description]

    All Others , 20.50 , [no description]

Slice Pies

    [no name] , [no price] , [no description]

    Cheese , [no price] , [no description]

    Pepperoni , [no price] , [no description]

    Porko , [no price] , [no description]

    Mushroom , [no price] , [no description]

    Pepperoni Mushroom , [no price] , [no description]

    Bronx Deluxe , [no price] , [no description]

    Veggie , [no price] , [no description]

    Sausage , [no price] , [no description]

    Primavera , [no price] , [no description]

    Artichoke , [no price] , [no description]

    Tomato Garlic , [no price] , [no description]

    Eggplant , [no price] , [no description]

    Pesto , [no price] , [no description]

    Whitestone , [no price] , [no description]

    Whitestone Spinach , [no price] , [no description]

    Whitestone Mushroom , [no price] , [no description]

    Whitestone Pepperoni , [no price] , [no description]

Calzone‏

    [no name] , [no price] , [no description]

    Calzone , 60.50 , [no description]

18" Whole Pies

    Cheese Pizza , 130.50 , [no description]

Specialty Pies‏

    Whitestone , 15.00 , Mozzarella, ricotta, garlic and parmesan.

    Primavera , 180.50 , Broccoli, spinach, peppers, mushrooms and garlic.

    Bronx Deluxe , 190.50 , Pepperoni, sausage, green peppers, black olives, onions, mushrooms and garlic.

    Porko , 18.00 , Pepperoni, sausage and meatballs.

**Is there a Python wrapper for the API?**

Yes, check this out: [https://github.com/Locu-Unofficial/locu-python](https://github.com/Locu-Unofficial/locu-python)

**How would I query venues in a geographic area with this wrapper?**

More details are available on the GitHub page, but here is a simple query using a latitude, longitude and radius:

 ![](data:image/*;base64,iVBORw0KGgoAAAANSUhEUgAAAlcAAAB3CAIAAAChavLMAAAAAXNSR0IArs4c6QAAAAlwSFlzAAAOwwAADsMBx2+oZAAAGxNJREFUeF7tnb9vI0eWx5uXG45uFwsYF4kTyIRx6TYjJ2dQkZIl9oLDZGRIYQFjJlCowMAAi2YoZRONQSdKhjxvMI7E82WHBWcCSdHZwGGc2fsH8F796q7qruru6h9sivw2FEjN6lfvfV6rXr+qZr3edrsNcIAACIAACIDAURL4p6O0GkaDAAiAAAiAACOAKIj7AARAAARA4HgJIAoer+9hOQiAAAiAQHdR8Nte8FL9vN+FIx7nwx4/hvPHXfRXr4/V1FNP4vnDvtoVo+9NV4Ql+XMHriCQ6hjOy/vEyj+RRYrPh9yYxBqrMd5+LK8iWoIACDRCgN6OMY/lmyCIoofa5zMC9BMfo20U5bZo68OHKAwt1rXV3YHLjSalDVxOQsPjUThZlr64bkPudaZB9r4uLXo5CQKlMsmj/z7dgFbvq52yKg0EDUHgMAgEVjPehcGLIHyXGTJ8z9sZvQm2L7SfOBxG/CT1+i7kDbQRVnwUn6QgSr9Hqtlmkm7vdo51tOJjmjiMoZkNfOIIIxE99eFPfFo8siZSksa8RxKqdaBoiy5KSRZmSlwcnThy+DCS4fadIMZ//6jBSnEWn1j9IrrQfzYF/xGEIYGrR6TYYG6zkCI5T2I+8tI8/jY5sTR2vdapN38Snhu1s/eV048+9koQ2gPvDp8dDmOIgxUgUEDAHgXFOBQFwQvz+b3KeasCrlxQxDMRF+l3MbDSKByP73RSfCpGYWrALuHxkoJB0UAshtdU3KIBMTlDQ7UyOfPsL1sZ42GZ/GK5jJMe6isexYx0go2MxvjmnVuQ+fpjSw4fFtXUEwZrpn63chbus/qFuaZ8LsjRKxN1bLpDGAYjECbBL/aRi79LDlNTdmzko378ixzt8pftfktutzL2avpjOAMBEGiegHtd8GQ2227/Ml687PXm+kKa73nfeduvHoLZjF30+XXweRD8Mg9+vwy+PJFi6OTvF8Ev/K8/RKwBHf967ttJ0v5xvhgs72ZK/uh6OVhwc1e3m2h7PRItT2Z3223Syq+7/v2VWpm6WBuXTpZJB6+jzS1fZ2rsyOHzH9eyl9/Ngq82Aa3L5nAWTVN+qaDlyWy8uWJsH+dXm7FETvzX64u+BNQnQOsPMYaYz8mzQUGHOXJW04vBOXfk6HxwIRbzxNEuf6vGTdlbgT8uAQEQsBHIezvml/nwr4vxN9vtLA4SXITv+eMmv5r2F+PMbCdnEp72O2ETBv/cSb/B7HKwePv4+HYxuOQPOnRQfEvPN6gnAy8d3XJWtzfBzZkIs2f0a/Ks4cO/fxos3nppZG/clL0NqAIRIAACjIAjCj7O570eC4F3arQSuHzP14dMycrHK5n8MWmr4OM4+F19uUpCnKDIE5QCijSF5Q3aW3/s9cA4jdjc87cx6TVBGlaNQ7xFqOUbj/ebMMl7nhvJ4PriefLWIoUGkbC0f6yDN9rbkn8fsJS6IueNdM37afByWqw5g9rvq9SMt09xLpZBLWz8XXJ4Tq8dWsrtw/+EIrjzfiiltGxUxd7Y4sC4DX26RVsQAAEXgcwkK3tH1PZqjO959+xt8goGf73ijVg1Wzrftki9iEGLf/EZulYsWcXv1DiXBrV3VCQL84U/BUhfndPemtFW7ZK3G+TrLdpCo+glvcKnZIeTSfJuIa1jiT/FoYS49bQTzXCjdb58PvRW0RvxYpF6HUlIznLO90u8Xph6lSl33r7o7SRJL2Ys3moxELn56/5iXtBbsnQ8ZstgV+Bvux9c/srzY1pP9TaQND5lr664eWs1v0ICiSBwfAR6ZDIeETohMB8Og9dV1xrraDwfBv9+12Q+XUeZ7q7tjH93JqNnEACBLAFEwW7uCvoGv5wcpVWx1LRzqxrNe8H/8Q7o3RnxFtJRHp3xP0raMBoE9pkAouA+ewe6gQAIgAAItEugux3U2rUL0kEABEAABECgmACiYDEjtAABEAABEDhUAoiCh+pZ2AUCIAACIFBMAFGwmBFagAAIgAAIHCoBRMFD9SzsAgEQAAEQKCaw6yiol5YzKrOp4n9xMTgqr0fqq/ZyFxfZSt8LstjGMi1W0+96vb951J8rI7Ram/nfer3vhvN/VLu64KrHD8Ped73pz60I14TuEc+2TYV8EACBJ00gGwVX36a2z5b2+Z63Y6FtqWVNAPqSHO1KJWq20XfH+Xlzs30mgW1jzbbzfy22MmUXUPtKO03m+ml0+um++HH2b9uoNWVOTu8ePk82rGnN5j3i2ZqNEAwCIHAIBLJRcPTn7faLRf9lb2iWLvc9X0yHEruzIBvSVlPKAin6xd8lH12PF32e/q2mdEFuCExyzSSpLF20/dNnidL/mA8pO1Q5mUih4mSRp2viR6aleo61+m/20fCDrPwuGtOfUoi6pBCQaq96kSrxfuO0NVdPZxe/CesS/VlLq/wgcOrvaJ90qvMstBYNQAAEQKATAs5N41qrL8hzQbZVYqrOn77pY3Z3U8oBw1QJvkb3u1v+GITvzbLCP030M9H3cnfQ6Hut5U+T4HtVGPZ9OPlJ6WReu6Vmi0C2/GmSNHOYEH0fRr9tH96HwSLZklScFAf7SPVLwq16uvBwsVIU/R5f65RPgmz657WnLTuzPBv1F4SBAAiAQCME3FV25QbL4YsgiGjvYfP4GPmd16+Oy4Ub5W2T+rdGKdTkQqNUeU7stkz3FZeDd0YjFYTiSPNbFP4YF81lly1/TCJKThRMh9hc71GgTaKmaEn9Uhw1fvQAmdHTLZ8in0XPXPmpQFuoTyO3JoSAAAiAwA4IdFNfUCzt0ZLfePEqU1l2dF1jX01eDjd9VN6yenYaXPGJzfmH4PJUVeLdSc4++ZdJ8GtSbzb45Nng02j7p632k0wNN6BnrnyLxb7tdwINnYAACICAL4GO6wvOLoMzxwuf82Hzb4L60gk+ux7//Gr183Tx2dey9t8ns/GvV9oLnKvbX8ezT6TgzW98LZAWzP4rVXfQt+fw9PR6+8fgLFlEHJ1/ehGvNabFZfX07ZDq/OXIt0jzbe+tEC4AARAAgV0QyCROvnUEXe3tiWxm8Y/XUqMpS7PkGre8uP7fDpJlviRm1AtMTU4ms4vJpGIYvWcLgXwWdDkxZzJLLArSzCebZaWlNTEFqi3d6ZOiplZZPW10+KIgE8LUEKt9BfLz9Jczt9JAU59d+AZ9gAAIgEBdAqgpUfSo8fN0+NvXd7udDi3Syfb5U9Gzim24BgRAAATaIoAo6CRLX3g4+1/56eSP2+vP2vJBTblPRc+aZuJyEAABEGiDAKJgG1QhEwRAAARA4GkQQBTswk/0+sx/ylLzZveT5Z+a2BenbfldMEOfIAACINAGAUTBNqhCJgiAAAiAwNMgsOvdtJ8GFWgJAiAAAiBwHAQQBY/Dz7ASBEAABEDARgBREPcFCIAACIDA8RJAFHT6Pi5PIWsbmg1X09KlKnZ/dyWVNfj+O3pRR1nooj2dCIw6eIXIkoeVZyKLfKA2E9oHv8yH8qZosl4myfIhVhIsmoEACBQQsO4dk90+m/ZAeWPbVtt9vu73+ffkeqPqYdM6seoaTctU8tKbkrfZV8YGTo1pkN6G3cNatquQuX2QDqtLv5gbu8t6mdyylM5GvcxQ1h7h9TIVF1NUuR3jPRiiKQiAQCEBe02Jd2HwIgjfZYYw3/PZ7vmGaexgA4H2B2up76KmhgxZgGKiLlPjYlyYQg49ep0mm5x8ELEipJZe61co5aoAlR7jffQ3jOVA8uOhbYe5dGmqlI3GkKqPvD56VuMsA4PWKd8gj+DGfswWVDbN0WOLdSu47vxCtqTisfiT2ah9oO4cS40UJSET9fg1hf+0aAACINAgAXdlpTbrC1qfhdOl5o1AKEcXPSYZ46Qx4JojbNGwksk5jOjmyjmy53315+Nme7kgD+BKvB4EffWswFl1bAQAHgj15M6wPc2zKJHszi/p0NVovUwSXiuBbnBogCgQOBIC7nXBk9lsu/3LePGy15vPtdUk3/OZGdmT2eXgQhZUml9tIlGt4XG+WK8v+nJJqU/fKV8ndYUmqsD8ybNBwQxvrhzbtavbTcTqPPGDF2aqVIipKf0d5iXrT/GqW69oYfJkNt5cMdc9EubxTBSGakrPHDmr6cXgnAMdnQ8u9MogsR8J9Otoc5upqtX8AkZT9saaPd5vMlrenJ0FSyoT1k8tIfOAlkw0aNeNrpfBeqBu6+SD0Wm4/vDQPAZIBAEQcBHopL7g6GsxArLh8lKOzhTf0klbpV1UmpLje8u03G+1uon0vLF4+/j4dkGYpUFN6emWs7q9CW7ORLA+o1+TWBee9ktj7Z8Gi7elW7sbNmVvrirt1ctsgABEgAAI5BLopr4gpYPB1TxJBFXeYH0bM0f/zT1PUilRouFWHiz/8JGTas9eS6xU2NC3X6GutIAeCCp2m39/M6X6fZWa8bZV9PThzHNr7dBSvvXF8+StUQrNImG0H3zGQPNjZUBV7M3zS+50RO16masPa59nBYxuIAAC9QlkZn7brS8Yd8deu8gsiplFBtnH8Zsc7A81tyRXTvRahfy1i3hFJSsnf4Jbb58spaXhik+yE1yJGX76G8LaWiC0rp/56Vmes96SvVplvAtF65GTCVsbFIdyVlme++MX/c7VLeb3WL16mXg75khWomDmPhHAPqL1HyQgoRQB+jZc8LrSmmsp8TtsRHnp7Xm8ltxgx60JblBHiAKBQyOAKHhoHt1Pe+bDniyiQau/d2qRcj91LaFVKxGdJvafB3dPH04JfmgCAntEAFFwj5wBVUAABEAABHZM4Dh2ULN+z4C9w1jpPZgduwjdgQAIgAAItEYAuWBraCEYBEAABEBg7wkcRy64926AgiAAAiAAAp0QQBTsBDs6BQEQAAEQ2AsCiIJ74QYoAQIgAAIg0AmBDqJgfn249ih01W+ORUZ1Oq0dfa9AHKU2wTHe/WnlfR9R5y+rjPV8rHx5E1wc2rsZIBkEQAAEBIFsFFx9m9o+W6LyPe8kLLbEtJYKcl2jCqzW8lqFfmv1V3QxhZD+Yiy2UHgYL+IYQ+cXY1HUakn7n5UKa8nOM5U2X81Vle1PR3tFZ/Z4cZ3XywuV8bKLQxE/fA4CIAACDRDIRsHRn7fbLxb9l73hD0Zdct/z/soZVcpV3zxNuFir7Znb+XKDlr7IoCOyk+k0LpxeEIwq1HwYXbPyFVlMdF7tsELbjidbjvkDbeYK9vRgi62u87O7pDXfx1sUs3AeLg7NaA8pIAACIJBLwD4j+uXd9puH8d/7vZfDZPtjkuN73hP+eVx4nYrUyLDDMzi9Dl/jyQ7FO5V7UfYVnHGTqVvKY25uKAniuVokahQ5j2o1H1hZDT5vSEmhbW+x1avFuJS97T4keLoxbk5VjXJ3zNbk5nOoqgCuAwEQAIEiAh3UF3Sq1L+/UsXz5G5bRdo38DkbqZdJBKK6b4NFHO/K1zWskAty5VkiJKY+06tuTOJZEFdEKhmBKYqXmkLNitMycemFioKSIFhQNkLXwc2hAR9DBAiAAAg4CXRSX9CqzWpKCZFYDvNcNdwH91bNBaXuPPgm5fRYBOQ0SiWCRjQ5n2zuKwGRcUjb6t2781S/HkFQXZniUMkQXAQCIAACHgS6qS9oUZBKeIdJPfTn6WTQUYdPJDB1kpa4ILvUicrjKTU8MFZpSpEuVnw1PbsZPBNS1Nsi1vILFoNJTpxHUlX5WI6UVZNPFcv4NfbpULv+Vg6Ve8aFIAACIOBBIFPmqe36gs56ctr7hLIQXfLmY3KRUYdPFXMrU6vKXcfOfJFRdJBX17BMb6XaaCpRpQVHFmwWHhSXpIsRJu/QxHLERKtRdbGUTtlGaXCqC9f52A5byUSr/jYOFZXFZSAAAiDgR+Bp7yMqXmw5iJp1Hg8u5ZuCT3lWaAkCIHCcBJ5yFKTVs/6HS/+1s2PxNPgci6dhJwiAQHUCTzkKVrcaV4IACIAACIAAI9DBDmoADwIgAAIgAAJ7QgBRsEVHiO/dtdgBRIMACIAACNQjgChYjx+uBgEQAAEQeMoEEAWfsvegOwiAAAiAQD0CiIL1+OFqEAABEACBp0zgaUVBvvOIucE3nSpVhG8HTnLX+Us+KbfNjW/7HRiHLkAABEDgIAl0UF+wBkfa6zK9Y4lWh6iG4KYutdb54zukis0MSm127du+KeUhBwRAAASOj0AH9QVFMT9K4FTGo/Ija31BcomWY+mplLV2vKwLuGKezFZCT+oIDukwikalXF+1RoTlDqKdSaPXso4gFQzc3HLl3Idv++O7aWExCIAACDRGoIP6gqxg4HKyvujLDGkZqLhgqy9IsSypNUGp1NmNst1aO17UBRRNWJUELXWkwBYXrVgO1utchhVrRJSp8+db88G3fWP3BgSBAAiAwOET6Ky+YBg9yErro2tZwsdaX1BkRrJc+eja3Pnayz8ns8vBRV98h+/sZkJFBXMur5IL6pGz1NSnl/poDAIgAAIg0DyBo6ovqJXQUzXlXUQr5oKxuJFe52/94UHrR1VQcjvTt33ztwUkggAIgMCRENj7+oKj88HFq3glbfWqVBV6WY2QErpkAjWY00rgo1c08rsHXHX+aC0wuJcdk/6D85Em11JvL7e9n0poDQIgAAIgUECg8/qC8WuVzvqC+muhk4komWes+EkTlaREUBhFSYW9pAgfa28rfudXlMrSOlXnT+hF7ZLz6W6L6gW2omZtOyEABEAABA6FAGpKtPicJDYRpVulxT4gGgRAAARAoAaBp/Wt+RqG4lIQAAEQAAEQyBBAFMRNAQIgAAIgcLwEEAWP1/ewHARAAARAAOuCuAdAAARAAASOlwByweP1PSwHARAAARBAFMQ9AAIgAAIgcLwEEAWP1/ewHARAAARAAFEQ9wAIgAAIgMDxEnha9QWP10+wHARAAARAoA0C9ndEfxj2vl+HXz3cfSmLOciufc+3oTFkggAIgAAIgEBTBDqoL9iU6pADAiAAAiAAAjUJFHxf8Jf58K8X6z9EDzNV4k/053u+ppa4HARAAARAAATaIJAXBVmoW4y/yVSj9T3fht6QCQIgAAIgAAL1CexNfcH6pkACCIAACIAACHgSyOaCq297Z/8TZF+N8T3vqQiagwAIgAAIgMDOCWAf0Z0jR4cgAAIgAAJ7QwDfmt8bV0AREAABEACBnRNAFNw5cnQIAiAAAiCwNwQQBffGFVAEBEAABEBg5wQQBXeOHB2CAAiAAAjsDQFEwb1xBRQBARAAARDYOQFEwZ0jR4cgAAIgAAJ7QwBRcG9cAUVAAARAAAR2TgBRcOfIu+7wcT7s8WM4f8zqspraz3etdcP9CwjTVYHY+TCBlM+tYf0y4nbjl32wtzHOJGg4b9svufLJaezfTG+zGz96Wt2Ont3zL41hmz6Wb4Igih5qn88IwIl9IvAQhaHFy82oGIWTZTOSWpRCBAq0XE6CTItD5lbb3kKi5d3ZCGebQeVVaKTlchJGjQhqWUgreu4B/1LYsrng6M/b7ReL/sve8AcjVfA9b4/D/KlDJSLaH6x1/BCoPUDJZ/apukw9vuvP8kKM5aE98yCmsiBqTUfec6Kui9TYkTwJO7u1y/XME2tFdPTHfGt75zO4j1+EEy/WN2eKWmG+RcrY/WLr12BtekQIodtAXZf07ORwH/dsUXN+dTM5H5V5nkz0N9NLe7/J2fRNa+WWkxtl+83/f4nvZOtkQFl7PfUvA7Bkm/L2CoGjr6PNVd100HlfWTmY45h+V1n9mDeO2f4vcsalvdKzQf4l741azZyx8iGKguBF9kHG93ymA+MpT3ta0JMTahOortnv6plcv9Z4lmePMjJ/zZETt6FuY/mlnhZKNOrKLpdqzEaVynCGRu7netbOnvf1C+njlRPoPep+cfW7XS7jRJPMMrI1dr3y7HIiPnJx0JnYaNgfZG18NLJ0kbpvnfzd+udwK9+v6/+l6BYua28Ofy+/5+vTkL3cH9mJrSIWmQkyy33l4KD3yG9HcwjN2uUax1z/F3m62+7/TvVsiL+vvzzbB/ntP0bhC9sEqe95s5fk/y0Z6fj/rnnI8S3nLklGwDgKuuWI8VAdBZNhFjGpMGIB15VdVh8WTHGUjYL+fvGNgna/5PjR/CgVBTNjnpOD676SNFkvlpskzc2QIoKuUMHN362/RxR09ru12lV8P5e0lyyrpL/nuMQ6ST+1md7Q/+Mt44Dqz+5FX220h+zkUiuHVEtuht5b+Sho/b8o8OPe6Bmb3Ax/X395ts97O0bWEdxuLSV2qe5g6fOZXJVNVNzSiwmr6cXgUpbvPXk2SOed16Vmo1LS8+SMrmM6y+Asd0b0ZHaXJXlnlhreG7tqTQYUXNyUX/K6sfnF2e9q2l+M1dO9dVBoE0d92d3oX+l+thrbjf71uTctYQccLP8X/n7sRs+mabcrr5v6giezy+BqPr/aRF/HkW50PriwvrWYA2Bzz5cuabL87EY1c8pJL4wNnjWOthO7HFakOLBFjDJLdNnQXsEvQSA9w9dL9W7FWoqhiMMvDj8+3m/CsXwaeZw/v1gXObEqBwrDRaLZ5yezMS09JSvoq9uNUM/Rb4H+Lm4ZVZz9llHa1qakvdX0t7jdU8+K9q4+rMPTfqav+vq4ODC3v4pfPV69Kr5BSTnbOEaL5eZwWG286lhPB39P57fePJPxsHdEXwThu/Rkuu/5gqTUOgFjzoqyeY74YZ/9oWY05VRJkgiEUSRm4OOlQZ2bnC/JCvfMm0s1371dOWrpJqtZI31aWFBKls/Muy2ZZ/LzC58OVKJSk4riA+Nkjl+sH2n5XziZsHl0Li5tl95HlkPefWWfTHNxy58hTIjG+jj0571auPn1W8Yu1w1jTl45+/XUPzar5Ppco/ZmJiSF7XK9rtR6ofO+cnIwFl4mammwjF3GOOY5Xu2lng7+pUbSHTZCfcHWnzPQwVMlQBnD7fm20sT8kzS5NXvp9UWaxS5aUGiemcugrvRp3sL9ltjaDdWw2YiCDQOFuEMiQLNSwevdj96dIWzFXlqw6H+43P3TBPX7PLi7m6VpdqVPZ17tqGMX/47UyekWUXD/fAKNQAAEQAAEdkUAO6jtinQb/Vi/Q5t5/aSNniETBEAABA6DAHLBw/AjrAABEAABEKhCALlgFWq4BgRAAARA4DAIIAoehh9hBQiAAAiAQBUCiIJVqOEaEAABEACBwyCAKHgYfoQVIAACIAACVQggClahhmtAAARAAAQOgwCi4GH4EVaAAAiAAAhUIfD/1xngCl7AVQIAAAAASUVORK5CYII=)

**Is there a limit on the number of venues can be retrieved?**

Yes, each call to the Search API will only return 25 venues. To iterate through all result sets (in groups of 25), you must use the following code:

 ![](data:image/*;base64,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)

**How would I access the menu information for a given venue using the wrapper?**

The following shows how to access the menus for a venue by using the "menus" property an an item in the list. Here the menus for the first item are accessed:

 ![](data:image/*;base64,iVBORw0KGgoAAAANSUhEUgAAAh8AAAAcCAIAAABONEoBAAAAAXNSR0IArs4c6QAAAAlwSFlzAAAOwwAADsMBx2+oZAAABKJJREFUeF7tnD1u2zAUgKWexc5k9AD2CZwpk9Gtmz3KKBA0Q8YMBQIU0uhsmVp4ymRv7RSfwMjQ5AS9hMofUaJkSaEcwnWST4vjB/L9fGL0HvmUhGmaBlwQgAAEIAABrwQ+eNWGMghAAAIQgIAkQHZhHUAAAhCAgH8CZBf/TNEIAQhAAAJkF9YABCAAAQj4J0B28c8UjRCAAAQgQHZhDUAAAhCAgH8CZBf/TNEIAQhAAAJkF9YABCAAAQj4J0B28c8UjRCAAAQgQHZhDexP4CkZhfIaJU+FEiMMw9naUr2e7Q7d3zIzIQCBYydQyS7rn2GY2I+KzP+u8mMPG/98ERjGj2l6H/WMvvWsv5yIfy8krlVwauWX8SJNH+OhL7vogQAEjpxAJbuMP6Xpx2X/Ihz9tqrRIOgqr4ta17SjkaphZ+usljXPn6LilaWwnq9ls5muetUsW66+aDV28ZzV08rWyKiqvQ22TWOiXIfb09r9D4LCrlW0a6Fwz9hqi7dprWSodJjWl4KR9v4l3Or4a3/cecrbcbeNbyM9cXweb+/s7Yvb78LxrRM3vxkFAQiUCegys3o9xnEQfB3GL5VX5qvadboSZe1UfwqB/EjTeKiKYHXJUcZ0PkPL80H5RFUkT215/rM0shtCfcBu0jb/hSkTgDBs25V+GE9W0/Z4m/ywY5f0tBZ/3Fr4t/AseaX3K8WtyG6YHdHu+Kbl97rXidtqYhQE3jaBhr5LL4rS9MtkeVE5KOsq383lw3gxVtLpmf7UBfhys5n3s/1Df74JNg950TtdZTN6J4Nna4NedDkwik5vpqv7rI6undht76JVNPk/EKbM8dB4sRos7fNF+YDWnowXMpjWeGtdVXFdaybJ1TY+V/B8cWvW04nns3enw4BjWicd3GYoBCBgCDR29f8mo+/Lybc0jYozdTmpq9wJtcgb1U1GllGcppcGyfP97BIH/60nY73ofrd2sHoI3Y07ztgnXnPOtJ7NB5fZPdlHT52LbXo68FSqNw+PlonBiSMSp2G+4tV53nmdOPnGIAhAoEygLrs8JUkYytRSKfy7yjuwHp8N5qUXjxzmbv+o1pDYgJze5MMT0WmxO0Z+n25NXvWiyfbKsiu6D5NyUq7M3CdesY0IrpJi46IekZ64NerpylPkwEDfF9GDuZ4PrA1q8y3VraTSG2YNg33FK5pJ/2OdOKxqhkDg7RAoF++rH6LdEgx/mQ5CvgvoKK87TsxfGBI9A9WKEOdFWmZaETbVrCujRaZVI3/O2gDF60fDOM60qT5EVYm3k812/8uvQ5m2iG65FJeR65ZJZ1elEVtF1nrxwK3Jn3Yna/soxZQdVxv6LpqSGf3a14m3BYciCLxuAqFw/+2kSiI5LAGxb/wc3LqfJXYdf9hosAYBCPgkwF9T+qT5DnWplzFcDjXl8Zd8X4MLAhB4HwTYu7yP+0yUEIAABA5LgL3LYXm3WKt9P9q13X00UeAIBCAAAUWAvQsLAQIQgAAE/BNg7+KfKRohAAEIQIDswhqAAAQgAAH/BMgu/pmiEQIQgAAEyC6sAQhAAAIQ8E+A7OKfKRohAAEIQOAf+4jSDEkQPMAAAAAASUVORK5CYII=)