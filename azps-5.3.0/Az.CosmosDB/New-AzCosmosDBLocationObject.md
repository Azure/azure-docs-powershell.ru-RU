---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508814"
---
# <span data-ttu-id="85459-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="85459-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="85459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85459-102">SYNOPSIS</span></span>
<span data-ttu-id="85459-103">Создайте новый объект расположения (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="85459-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="85459-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85459-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85459-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85459-105">DESCRIPTION</span></span>
<span data-ttu-id="85459-106">Создайте новый объект расположения (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="85459-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="85459-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85459-107">EXAMPLES</span></span>

### <span data-ttu-id="85459-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85459-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="85459-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85459-109">PARAMETERS</span></span>

### <span data-ttu-id="85459-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85459-110">-DefaultProfile</span></span>
<span data-ttu-id="85459-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85459-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85459-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="85459-112">-FailoverPriority</span></span>
<span data-ttu-id="85459-113">Приоритет от сбойного действия для расположения.</span><span class="sxs-lookup"><span data-stu-id="85459-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85459-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="85459-114">-IsZoneRedundant</span></span>
<span data-ttu-id="85459-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="85459-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85459-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="85459-116">-LocationName</span></span>
<span data-ttu-id="85459-117">Имя строки "Расположение".</span><span class="sxs-lookup"><span data-stu-id="85459-117">Name of the Location in string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85459-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85459-118">CommonParameters</span></span>
<span data-ttu-id="85459-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85459-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85459-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85459-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85459-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85459-121">INPUTS</span></span>

### <span data-ttu-id="85459-122">Нет</span><span class="sxs-lookup"><span data-stu-id="85459-122">None</span></span>

## <span data-ttu-id="85459-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85459-123">OUTPUTS</span></span>

### <span data-ttu-id="85459-124">Microsoft.Azure.Commands.ВацDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="85459-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="85459-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85459-125">NOTES</span></span>

## <span data-ttu-id="85459-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85459-126">RELATED LINKS</span></span>
