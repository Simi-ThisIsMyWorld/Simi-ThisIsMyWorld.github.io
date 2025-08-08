# Simi-ThisIsMyWorld.github.io
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BioDiversity Builders 2025 - Everything about Native plants</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        .header {
            background: linear-gradient(135deg, #2c5f41, #4a8b3a);
            color: white;
            padding: 1.5rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            color: #2c5f41;
        }

        .search-container {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .search-box {
            padding: 0.75rem 1rem;
            border: none;
            border-radius: 25px;
            width: 300px;
            font-size: 14px;
        }

        .search-btn {
            background: rgba(255,255,255,0.2);
            border: 1px solid rgba(255,255,255,0.3);
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s;
        }

        .search-btn:hover {
            background: rgba(255,255,255,0.3);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            display: grid;
            grid-template-columns: 250px 1fr;
            gap: 2rem;
        }

        .sidebar {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            height: fit-content;
            position: sticky;
            top: 2rem;
        }

        .sidebar h3 {
            color: #2c5f41;
            margin-bottom: 1rem;
            font-size: 16px;
            border-bottom: 2px solid #4a8b3a;
            padding-bottom: 0.5rem;
        }

        .filter-group {
            margin-bottom: 1.5rem;
        }

        .filter-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: #555;
        }

        .filter-group select, .filter-group input {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 14px;
        }

        .main-content {
            background: white;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .welcome-section {
            padding: 2rem;
            border-bottom: 1px solid #eee;
        }

        .welcome-section h1 {
            color: #2c5f41;
            margin-bottom: 1rem;
            font-size: 2.5rem;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }

        .stat-card {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            border-left: 4px solid #4a8b3a;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: #2c5f41;
        }

        .stat-label {
            font-size: 0.9rem;
            color: #666;
            margin-top: 0.5rem;
        }

        .plant-grid {
            padding: 2rem;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .plant-card {
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.3s;
            cursor: pointer;
            background: white;
        }

        .plant-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .plant-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(45deg, #4a8b3a, #6db86d);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
            position: relative;
        }

        .plant-info {
            padding: 1.5rem;
        }

        .plant-name {
            font-size: 1.3rem;
            font-weight: bold;
            color: #2c5f41;
            margin-bottom: 0.5rem;
        }

        .plant-scientific {
            font-style: italic;
            color: #666;
            margin-bottom: 1rem;
        }

        .plant-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .tag {
            background: #e8f5e8;
            color: #2c5f41;
            padding: 0.25rem 0.75rem;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid #4a8b3a;
        }

        .plant-description {
            color: #555;
            font-size: 0.9rem;
            line-height: 1.5;
        }

        .plant-detail {
            display: none;
            padding: 2rem;
        }

        .plant-detail.active {
            display: block;
        }

        .detail-header {
            display: flex;
            align-items: center;
            gap: 2rem;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 2px solid #4a8b3a;
        }

        .detail-image {
            width: 300px;
            height: 200px;
            background: linear-gradient(45deg, #4a8b3a, #6db86d);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 4rem;
        }

        .detail-info h1 {
            color: #2c5f41;
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .detail-scientific {
            font-style: italic;
            color: #666;
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .detail-sections {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .detail-section {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 10px;
            border-left: 4px solid #4a8b3a;
        }

        .detail-section h2 {
            color: #2c5f41;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .back-btn {
            background: #4a8b3a;
            color: white;
            border: none;
            padding: 0.75rem 1.5rem;
            border-radius: 5px;
            cursor: pointer;
            margin-bottom: 2rem;
            transition: background 0.3s;
        }

        .back-btn:hover {
            background: #2c5f41;
        }

        .no-results {
            text-align: center;
            padding: 3rem;
            color: #666;
        }

        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
                padding: 1rem;
            }
            
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }
            
            .search-box {
                width: 250px;
            }
            
            .detail-header {
                flex-direction: column;
                text-align: center;
            }
            
            .detail-sections {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="header-content">
            <div class="logo">
                <div class="logo-icon">🌿</div>
                <div>
                    <h1>BioDiversity Builders 2025</h1>
                    <p>Everything about Native plants</p>
                </div>
            </div>
            <div class="search-container">
                <input type="text" class="search-box" placeholder="Search native plants..." id="searchInput">
                <button class="search-btn" onclick="searchPlants()">Search</button>
            </div>
        </div>
    </header>

    <div class="container">
        <aside class="sidebar">
            <h3>Filter Plants</h3>
            
            <div class="filter-group">
                <label for="habitatFilter">Habitat</label>
                <select id="habitatFilter" onchange="filterPlants()">
                    <option value="">All Habitats</option>
                    <option value="woodland">Woodland</option>
                    <option value="wetland">Wetland</option>
                    <option value="meadow">Meadow</option>
                    <option value="coastal">Coastal</option>
                    <option value="prairie">Prairie</option>
                </select>
            </div>

            <div class="filter-group">
                <label for="bloomFilter">Bloom Time</label>
                <select id="bloomFilter" onchange="filterPlants()">
                    <option value="">All Seasons</option>
                    <option value="spring">Spring</option>
                    <option value="summer">Summer</option>
                    <option value="fall">Fall</option>
                </select>
            </div>

            <div class="filter-group">
                <label for="typeFilter">Plant Type</label>
                <select id="typeFilter" onchange="filterPlants()">
                    <option value="">All Types</option>
                    <option value="tree">Tree</option>
                    <option value="shrub">Shrub</option>
                    <option value="perennial">Perennial</option>
                    <option value="annual">Annual</option>
                    <option value="fern">Fern</option>
                    <option value="grass">Grass</option>
                </select>
            </div>

            <div class="filter-group">
                <label for="sunFilter">Sun Requirements</label>
                <select id="sunFilter" onchange="filterPlants()">
                    <option value="">All Light Conditions</option>
                    <option value="full-sun">Full Sun</option>
                    <option value="partial-shade">Partial Shade</option>
                    <option value="full-shade">Full Shade</option>
                </select>
            </div>
        </aside>

        <main class="main-content">
            <section class="welcome-section" id="welcomeSection">
                <h1>Welcome to BioDiversity Builders 2025</h1>
                <p>Transform your landscape into a wildlife haven! Based on research by Dr. Doug Tallamy and conservation organizations, native plants are the foundation of healthy ecosystems. Every native plant you choose supports local food webs, from caterpillars that feed baby birds to berries that sustain wildlife through winter.</p>
                
                <div class="stats">
                    <div class="stat-card">
                        <div class="stat-number">530+</div>
                        <div class="stat-label">Caterpillars on Oak</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">96%</div>
                        <div class="stat-label">Birds Need Insects</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">40+</div>
                        <div class="stat-label">Birds Eat Elderberries</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">29x</div>
                        <div class="stat-label">More Wildlife Than Non-natives</div>
                    </div>
                </div>

                <p><strong>Why Native Plants Matter:</strong> Non-native ornamentals support 29 times less animal diversity than natives. By choosing plants that co-evolved with our local wildlife, you become part of the solution to biodiversity loss and help create corridors of habitat where animals can thrive alongside humans.</p>
            </section>

            <div class="plant-grid" id="plantGrid">
                <!-- Plants will be populated by JavaScript -->
            </div>

            <div class="plant-detail" id="plantDetail">
                <button class="back-btn" onclick="showPlantGrid()">← Back to Plant List</button>
                <div id="plantDetailContent">
                    <!-- Plant detail content will be populated by JavaScript -->
                </div>
            </div>
        </main>
    </div>

    <script>
        const plants = [
            {
                id: 1,
                name: "Northern Red Oak",
                scientific: "Quercus rubra",
                type: "tree",
                habitat: "woodland",
                bloom: "spring",
                sun: "full-sun",
                image: "🌳",
                tags: ["Keystone Species", "530+ Caterpillars", "Acorns for Wildlife"],
                description: "A keystone species supporting over 530 species of moths and butterflies. Essential for birds, providing acorns for jays, woodpeckers, and countless other wildlife.",
                details: {
                    identification: "Large deciduous tree 60-75 feet tall with distinctive lobed leaves having pointed tips. Bark becomes deeply furrowed with age.",
                    pollinators: "Wind-pollinated tree that produces abundant pollen in spring. Early pollen supports native bees including Andrena species, Halictus bees, and other spring-active pollinators during critical early season when few other resources are available.",
                    habitat: "Well-drained upland forests throughout Massachusetts. Dominant canopy species in many mixed hardwood forests.",
                    ecology: "Supports more caterpillar species than almost any other tree - crucial protein source for nesting birds. Acorns feed squirrels, chipmunks, turkeys, jays, and woodpeckers. Wind-pollinated flowers provide pollen for early spring bees.",
                    wildlife: "Keystone species supporting 530+ moth and butterfly species. Provides acorns for mammals and birds, nesting sites for cavity nesters, and shelter for countless wildlife species.",
                    cultivation: "Excellent shade tree for large properties. Needs space to reach full potential. Plant for future generations - can live 300+ years."
                }
            },
            {
                id: 2,
                name: "Eastern White Pine",
                scientific: "Pinus strobus",
                type: "tree",
                habitat: "woodland",
                bloom: "spring",
                sun: "full-sun",
                image: "🌲",
                tags: ["State Tree", "Finch Food", "Year-round Shelter"],
                description: "Massachusetts' state tree provides seeds for finches, siskins, and chickadees. Offers year-round shelter and nesting sites for countless birds.",
                details: {
                    identification: "Majestic evergreen up to 100+ feet with soft, blue-green needles in clusters of 5. Distinctive whorled branching pattern.",
                    habitat: "Sandy, well-drained soils throughout Massachusetts. From coastal areas to mountain slopes in mixed and pure stands.",
                    ecology: "Seeds eaten by finches, siskins, chickadees, and nuthatches. Dense canopy provides critical winter shelter. Woodpeckers excavate nest cavities. Wind-pollinated; pollen supports early spring native bees.",
                    cultivation: "Needs full sun and well-drained soil. Fast-growing when young. Susceptible to white pine weevil and blister rust."
                }
            },
            {
                id: 3,
                name: "American Elderberry",
                scientific: "Sambucus canadensis",
                type: "shrub",
                habitat: "wetland",
                bloom: "summer",
                sun: "partial-shade",
                image: "🫐",
                tags: ["40+ Bird Species", "Edible Berries", "Fast Growing"],
                description: "A wildlife magnet whose berries feed over 40 bird species. White flower clusters attract beneficial insects in summer, berries sustain birds through fall.",
                details: {
                    identification: "Large shrub 5-12 feet tall with compound leaves and flat-topped clusters of creamy white flowers followed by dark purple berries.",
                    pollinators: "Primary pollinators include native bees (Halictus, Lasioglossum species), syrphid flies, small butterflies, and beneficial wasps. Flat flower clusters provide easy landing platforms for diverse pollinators.",
                    habitat: "Moist soils along streams, wetlands, and forest edges. Tolerates seasonal flooding and various soil types.",
                    ecology: "Berries eaten by cardinals, grosbeaks, tanagers, thrushes, and 35+ other bird species. Flowers provide nectar for native bees, syrphid flies, and small butterflies. Important early summer pollinator resource.",
                    wildlife: "Feeds 40+ bird species with nutritious berries. Flowers support diverse native pollinators and beneficial insects. Dense growth provides nesting sites for songbirds.",
                    cultivation: "Fast-growing, easy to establish. Berries edible for humans too - great for jams and jellies. May sucker to form colonies."
                }
            },
            {
                id: 4,
                name: "Allegheny Serviceberry",
                scientific: "Amelanchier laevis",
                type: "shrub",
                habitat: "woodland",
                bloom: "spring",
                sun: "partial-shade",
                image: "🌸",
                tags: ["Early Blooms", "Bird Berries", "Four Season Interest"],
                description: "Early white flowers feed spring pollinators, nutritious berries sustain thrushes, orioles, and warblers. Spectacular fall color and winter bark interest.",
                details: {
                    identification: "Small tree or large shrub 15-25 feet with oval leaves and clusters of white flowers in early spring before leaves emerge.",
                    pollinators: "Critical early spring pollinator plant supporting native bees including Andrena species, Osmia mason bees, and Halictus sweat bees. Also attracts beneficial hover flies and early butterflies during peak bloom.",
                    habitat: "Rocky slopes, forest edges, and well-drained woodlands. Tolerates various soil conditions from acid to neutral.",
                    ecology: "Berries eaten by 40+ bird species including thrushes, orioles, warblers, and cedar waxwings. Early flowers crucial for native bees, especially Andrena and Osmia species. Flowers also attract beneficial hover flies.",
                    wildlife: "Berries feed thrushes, warblers, orioles, and 35+ other bird species. Early blooms provide critical nectar when few other flowers available. Dense branching offers nesting sites.",
                    cultivation: "Excellent four-season plant. Drought tolerant once established. Can be grown as single or multi-stemmed specimen."
                }
            },
            {
                id: 5,
                name: "Native Sunflowers",
                scientific: "Helianthus species",
                type: "perennial",
                habitat: "meadow",
                bloom: "summer",
                sun: "full-sun",
                image: "🌻",
                tags: ["Seed Source", "Pollinator Magnet", "Goldfinch Favorite"],
                description: "Living bird feeders! Seeds feed cardinals, finches, and sparrows. Massive flower heads attract countless bees and butterflies throughout summer.",
                details: {
                    identification: "Tall perennials 4-8 feet with large, heart-shaped leaves and distinctive yellow flower heads with dark centers.",
                    pollinators: "Attracts long-horned bees (Melissodes, Eucera species), leafcutter bees, sweat bees, bumble bees, and numerous butterflies including painted ladies, skippers, and sulphurs. Excellent late-season pollinator resource.",
                    habitat: "Open meadows, prairies, and disturbed areas. Prefers full sun and well-drained to moderately moist soils.",
                    ecology: "Seeds provide high-energy food for numerous songbirds. Flowers attract native bees (especially long-horned bees), beneficial insects, and butterflies including painted ladies and skippers. Nesting material from stems.",
                    wildlife: "Seeds feed cardinals, finches, nuthatches, and sparrows. Massive flower heads support dozens of pollinator species. Stems provide nesting material for native bees.",
                    cultivation: "Low maintenance once established. May need staking in windy areas. Leave seed heads standing for winter bird food."
                }
            },
            {
                id: 6,
                name: "Paper Birch",
                scientific: "Betula papyrifera",
                type: "tree",
                habitat: "woodland",
                bloom: "spring",
                sun: "full-sun",
                image: "🌿",
                tags: ["200+ Caterpillars", "Chickadee Food", "Distinctive Bark"],
                description: "Supports over 200 caterpillar species - essential protein for chickadees and other insect-eating birds. Distinctive white bark provides year-round beauty.",
                details: {
                    identification: "Medium tree 40-70 feet with distinctive white, papery bark that peels in sheets. Yellow fall color and triangular leaves.",
                    pollinators: "Wind-pollinated with separate male and female catkins. Male catkins provide early pollen for native bees, especially Andrena species and other spring-active bees when few other resources exist.",
                    habitat: "Cool, moist sites throughout Massachusetts. Common in northern forests, mountain slopes, and areas with good drainage.",
                    ecology: "Hosts hundreds of caterpillar species crucial for nesting birds. Seeds eaten by finches, siskins, and redpolls. Bark used by birds for nesting. Wind-pollinated but catkins provide early pollen for bees.",
                    wildlife: "Supports 200+ caterpillar species feeding birds. Seeds eaten by finches and siskins. Bark strips used by birds for nest construction. Provides browsing for wildlife.",
                    cultivation: "Prefers cool, moist conditions. May struggle in hot, dry locations. Excellent specimen tree for naturalistic landscapes."
                }
            },
            {
                id: 7,
                name: "Wild Black Cherry",
                scientific: "Prunus serotina",
                type: "tree",
                habitat: "woodland",
                bloom: "spring",
                sun: "full-sun",
                image: "🍒",
                tags: ["Bird Cherries", "Woodpecker Tree", "Spring Flowers"],
                description: "Spring flowers feed early pollinators, cherries sustain 40+ bird species. Mature trees provide nesting cavities excavated by woodpeckers.",
                details: {
                    identification: "Medium to large tree 50-80 feet with distinctive dark, scaly bark. White flower clusters in spring followed by dark red cherries.",
                    pollinators: "Specialized native bees include Andrena species (cherry specialists), plus Halictus sweat bees, Osmia mason bees, and various butterflies including spring azure and mourning cloak.",
                    habitat: "Forest edges, clearings, and disturbed areas. Adaptable to various soil conditions from dry to moderately moist.",
                    ecology: "Cherries eaten by thrushes, vireos, flycatchers, and many other songbirds. Flowers provide early nectar for native bees, including specialist cherry bees (Andrena species). Bark and leaves host various caterpillars.",
                    wildlife: "Cherries feed 40+ bird species including thrushes, vireos, and woodpeckers. Provides nesting sites and supports numerous caterpillar species for insect-eating birds.",
                    cultivation: "Fast-growing pioneer species. Self-seeds readily. Excellent for naturalized areas and wildlife gardens."
                }
            },
            {
                id: 8,
                name: "New England Aster",
                scientific: "Symphyotrichum novae-angliae",
                type: "perennial",
                habitat: "meadow",
                bloom: "fall",
                sun: "full-sun",
                image: "💜",
                tags: ["Monarch Fuel", "Late Season Bloomer", "Finch Seeds"],
                description: "Critical late-season nectar for migrating monarchs and other butterflies. Seeds provide fall and winter food for goldfinches and sparrows.",
                details: {
                    identification: "Tall perennial 3-6 feet with lance-shaped leaves and masses of purple, daisy-like flowers with yellow centers in fall.",
                    pollinators: "Essential for migrating monarch butterflies, plus native bees, beneficial wasps, painted lady butterflies, skippers, and late-season active pollinators when few other nectar sources remain available.",
                    habitat: "Meadows, prairies, and open areas. Thrives in full sun with medium to moist soils throughout Massachusetts.",
                    ecology: "Essential late-season nectar source for monarchs preparing for migration. Seeds eaten by goldfinches, sparrows, and other songbirds. Flowers attract native bees, butterflies, and beneficial wasps.",
                    wildlife: "Critical fuel stop for migrating monarchs. Seeds feed goldfinches, juncos, and sparrows. Late flowers support bees preparing for winter.",
                    cultivation: "May self-seed extensively. Can be cut back mid-season to reduce height. Excellent for pollinator gardens and naturalized areas."
                }
            },
            {
                id: 9,
                name: "Staghorn Sumac",
                scientific: "Rhus typhina",
                type: "shrub",
                habitat: "meadow",
                bloom: "summer",
                sun: "full-sun",
                image: "🔥",
                tags: ["Winter Bird Food", "Brilliant Fall Color", "Drought Tolerant"],
                description: "Brilliant red fall foliage and persistent red berry clusters provide crucial winter food for chickadees, titmice, and other birds during harsh weather.",
                details: {
                    identification: "Large shrub or small tree 15-25 feet with compound leaves and dense, cone-shaped clusters of red berries. Velvety twigs.",
                    pollinators: "Small greenish flowers attract native bees, beneficial wasps, syrphid flies, and various small pollinators. Particularly valuable for specialist native bees and beneficial insects in summer.",
                    habitat: "Open areas, forest edges, and disturbed sites. Extremely adaptable to poor soils and drought conditions.",
                    ecology: "Red berries persist through winter, providing essential food when other sources are scarce. Forms colonies that provide cover for wildlife. Small flowers attract native bees and beneficial insects in summer.",
                    wildlife: "Berries sustain 35+ bird species through winter including chickadees, woodpeckers, and game birds. Dense colonies provide shelter and nesting sites.",
                    cultivation: "Extremely low maintenance and drought tolerant. Suckers to form colonies. Excellent for erosion control and difficult sites."
                }
            },
            {
                id: 10,
                name: "Wild Bergamot",
                scientific: "Monarda fistulosa",
                type: "perennial",
                habitat: "meadow",
                bloom: "summer",
                sun: "full-sun",
                image: "🌺",
                tags: ["Hummingbird Plant", "Native Bee Magnet", "Aromatic Leaves"],
                description: "Aromatic mint family member with lavender flowers that attract hummingbirds, native bees, and butterflies. Traditional medicinal and tea plant.",
                details: {
                    identification: "Square-stemmed perennial 2-4 feet tall with opposite, aromatic leaves and dense clusters of tubular lavender flowers.",
                    pollinators: "Primary pollinators include ruby-throated hummingbirds, bumblebees, long-tongued bees, skippers, clearwing moths, and various butterflies. Tubular flowers perfectly designed for long-tongued pollinators.",
                    habitat: "Prairies, meadows, and woodland edges throughout Massachusetts. Prefers well-drained soils and full sun.",
                    ecology: "Major nectar source for hummingbirds, native bees (especially bumblebees), and butterflies including skippers and clearwing moths. Forms colonies through underground rhizomes, creating habitat patches.",
                    wildlife: "Essential nectar source for hummingbirds and specialized long-tongued bees. Dense colonies provide cover for small wildlife and beneficial insects.",
                    cultivation: "Drought tolerant once established. Can spread in favorable conditions. Excellent for butterfly gardens and naturalized plantings."
                }
            },
            {
                id: 11,
                name: "Winterberry Holly",
                scientific: "Ilex verticillata",
                type: "shrub",
                habitat: "wetland",
                bloom: "spring",
                sun: "partial-shade",
                image: "🔴",
                tags: ["Winter Bird Food", "Wetland Native", "Brilliant Berries"],
                description: "Bright red berries persist through winter, providing crucial food for robins, cedar waxwings, and bluebirds when other food sources are scarce.",
                details: {
                    identification: "Deciduous shrub 6-10 feet tall with serrated leaves. Female plants produce masses of bright red berries on bare winter branches.",
                    pollinators: "Small white flowers attract native bees including Halictus sweat bees, Lasioglossum species, Andrena mining bees, and various beneficial flies. Important early summer nectar source in wetland habitats.",
                    habitat: "Wet soils in swamps, marshes, and stream borders. Tolerates seasonal flooding and acidic conditions throughout Massachusetts.",
                    ecology: "Berries are critical winter food for 40+ bird species including thrushes, waxwings, and woodpeckers. Small white flowers provide nectar for native bees, especially Halictus and Lasioglossum species.",
                    wildlife: "Berries sustain 40+ bird species through winter when other food is scarce. Dense growth provides nesting sites for wetland birds.",
                    cultivation: "Needs both male and female plants for berry production. Excellent for rain gardens and wet sites. Outstanding winter interest."
                }
            },
            {
                id: 12,
                name: "Wild Columbine",
                scientific: "Aquilegia canadensis",
                type: "perennial",
                habitat: "woodland",
                bloom: "spring",
                sun: "partial-shade",
                image: "🌹",
                tags: ["Hummingbird Flower", "Spring Ephemeral", "Shade Garden"],
                description: "Delicate red and yellow flowers perfectly designed for hummingbird pollination. Early spring blooms provide nectar when few other flowers are available.",
                details: {
                    identification: "Graceful perennial 1-3 feet tall with delicate, divided leaves and distinctive spurred flowers in red and yellow.",
                    habitat: "Rocky woodlands, cliff faces, and shaded slopes. Prefers well-drained, slightly alkaline soils with consistent moisture.",
                    ecology: "Primary pollinator is ruby-throated hummingbird, though long-tongued bees and sphinx moths also visit. Specialized flower shape co-evolved with hummingbirds. Self-seeds in favorable conditions.",
                    cultivation: "Excellent for shade gardens and woodland settings. Short-lived but self-seeds. Prefers cool, moist conditions."
                }
            }
        ];

        let filteredPlants = [...plants];
        let currentView = 'grid';

        function renderPlants() {
            const plantGrid = document.getElementById('plantGrid');
            
            if (filteredPlants.length === 0) {
                plantGrid.innerHTML = '<div class="no-results"><h2>No plants found</h2><p>Try adjusting your search criteria or filters.</p></div>';
                return;
            }

            plantGrid.innerHTML = filteredPlants.map(plant => `
                <div class="plant-card" onclick="showPlantDetail(${plant.id})">
                    <div class="plant-image">${plant.image}</div>
                    <div class="plant-info">
                        <div class="plant-name">${plant.name}</div>
                        <div class="plant-scientific">${plant.scientific}</div>
                        <div class="plant-tags">
                            ${plant.tags.map(tag => `<span class="tag">${tag}</span>`).join('')}
                        </div>
                        <div class="plant-description">${plant.description}</div>
                    </div>
                </div>
            `).join('');
        }

        function showPlantDetail(id) {
            const plant = plants.find(p => p.id === id);
            if (!plant) return;

            const detailContent = document.getElementById('plantDetailContent');
            detailContent.innerHTML = `
                <div class="detail-header">
                    <div class="detail-image">${plant.image}</div>
                    <div class="detail-info">
                        <h1>${plant.name}</h1>
                        <div class="detail-scientific">${plant.scientific}</div>
                        <div class="plant-tags">
                            ${plant.tags.map(tag => `<span class="tag">${tag}</span>`).join('')}
                        </div>
                    </div>
                </div>
                
                <div class="detail-sections">
                    <div class="detail-section">
                        <h2>Identification</h2>
                        <p>${plant.details.identification}</p>
                    </div>
                    <div class="detail-section">
                        <h2>Key Pollinators</h2>
                        <p>${plant.details.pollinators}</p>
                    </div>
                    <div class="detail-section">
                        <h2>Habitat & Distribution</h2>
                        <p>${plant.details.habitat}</p>
                    </div>
                    <div class="detail-section">
                        <h2>Ecological Value</h2>
                        <p>${plant.details.ecology}</p>
                    </div>
                    <div class="detail-section">
                        <h2>Wildlife Benefits</h2>
                        <p>${plant.details.wildlife}</p>
                    </div>
                    <div class="detail-section">
                        <h2>Cultivation Notes</h2>
                        <p>${plant.details.cultivation}</p>
                    </div>
                </div>
            `;

            document.getElementById('welcomeSection').style.display = 'none';
            document.getElementById('plantGrid').style.display = 'none';
            document.getElementById('plantDetail').classList.add('active');
            currentView = 'detail';
        }

        function showPlantGrid() {
            document.getElementById('welcomeSection').style.display = 'block';
            document.getElementById('plantGrid').style.display = 'grid';
            document.getElementById('plantDetail').classList.remove('active');
            currentView = 'grid';
        }

        function filterPlants() {
            const habitat = document.getElementById('habitatFilter').value;
            const bloom = document.getElementById('bloomFilter').value;
            const type = document.getElementById('typeFilter').value;
            const sun = document.getElementById('sunFilter').value;
            const search = document.getElementById('searchInput').value.toLowerCase();

            filteredPlants = plants.filter(plant => {
                return (!habitat || plant.habitat === habitat) &&
                       (!bloom || plant.bloom === bloom) &&
                       (!type || plant.type === type) &&
                       (!sun || plant.sun === sun) &&
                       (!search || plant.name.toLowerCase().includes(search) || 
                        plant.scientific.toLowerCase().includes(search) ||
                        plant.tags.some(tag => tag.toLowerCase().includes(search)));
            });

            if (currentView === 'grid') {
                renderPlants();
            }
        }

        function searchPlants() {
            filterPlants();
        }

        // Event listener for real-time search
        document.getElementById('searchInput').addEventListener('input', filterPlants);

        // Initialize the page
        renderPlants();
    </script>
</body>
</html>
