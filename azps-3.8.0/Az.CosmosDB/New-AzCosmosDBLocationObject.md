---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073646"
---
# <span data-ttu-id="f656a-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="f656a-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="f656a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f656a-102">SYNOPSIS</span></span>
<span data-ttu-id="f656a-103">Создайте новый объект расположения CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="f656a-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="f656a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f656a-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f656a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f656a-105">DESCRIPTION</span></span>
<span data-ttu-id="f656a-106">Создайте новый объект расположения CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="f656a-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="f656a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f656a-107">EXAMPLES</span></span>

### <span data-ttu-id="f656a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f656a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="f656a-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f656a-109">PARAMETERS</span></span>

### <span data-ttu-id="f656a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f656a-110">-DefaultProfile</span></span>
<span data-ttu-id="f656a-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f656a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f656a-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="f656a-112">-FailoverPriority</span></span>
<span data-ttu-id="f656a-113">Приоритет перемещения при переходе на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="f656a-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="f656a-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="f656a-114">-IsZoneRedundant</span></span>
<span data-ttu-id="f656a-115">Логическое значение, указывающее, является ли эта область AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="f656a-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="f656a-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="f656a-116">-LocationName</span></span>
<span data-ttu-id="f656a-117">Имя расположения в строке.</span><span class="sxs-lookup"><span data-stu-id="f656a-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="f656a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f656a-118">CommonParameters</span></span>
<span data-ttu-id="f656a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f656a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f656a-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f656a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f656a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f656a-121">INPUTS</span></span>

### <span data-ttu-id="f656a-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="f656a-122">None</span></span>

## <span data-ttu-id="f656a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f656a-123">OUTPUTS</span></span>

### <span data-ttu-id="f656a-124">Microsoft. Azure. Commands. CosmosDB. Models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="f656a-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="f656a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f656a-125">NOTES</span></span>

## <span data-ttu-id="f656a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f656a-126">RELATED LINKS</span></span>
