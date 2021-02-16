---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 063abe34cbbd6c0f10e275e5b4b63f3c163b87e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213220"
---
# <span data-ttu-id="ee923-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="ee923-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="ee923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee923-102">SYNOPSIS</span></span>
<span data-ttu-id="ee923-103">Получить доступную информацию о SKU местоположения</span><span class="sxs-lookup"><span data-stu-id="ee923-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="ee923-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee923-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ee923-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee923-105">DESCRIPTION</span></span>
<span data-ttu-id="ee923-106">Получить доступную информацию о SKU местоположения</span><span class="sxs-lookup"><span data-stu-id="ee923-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="ee923-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee923-107">EXAMPLES</span></span>

### <span data-ttu-id="ee923-108">Пример 1. Просмотр возможностей расположения по имени расположения</span><span class="sxs-lookup"><span data-stu-id="ee923-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location eastus

SKU              Tier            Memory vCore
---              ----            ------ -----
Standard_B1ms    Burstable         2048     1
Standard_B2s     Burstable         2048     2
Standard_D2s_v3  GeneralPurpose    4096     2
Standard_D4s_v3  GeneralPurpose    4096     4
Standard_D8s_v3  GeneralPurpose    4096     8
Standard_D16s_v3 GeneralPurpose    4096    16
Standard_D32s_v3 GeneralPurpose    4096    32
Standard_D48s_v3 GeneralPurpose    4096    48
Standard_D64s_v3 GeneralPurpose    4096    64
Standard_E2s_v3  MemoryOptimized   8192     2
Standard_E4s_v3  MemoryOptimized   8192     4
Standard_E8s_v3  MemoryOptimized   8192     8
Standard_E16s_v3 MemoryOptimized   8192    16
Standard_E32s_v3 MemoryOptimized   8192    32
Standard_E48s_v3 MemoryOptimized   8192    48
Standard_E64s_v3 MemoryOptimized   6912    64
```

<span data-ttu-id="ee923-109">Этот cmdlet shows basic sku of the provided location.</span><span class="sxs-lookup"><span data-stu-id="ee923-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="ee923-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee923-110">PARAMETERS</span></span>

### <span data-ttu-id="ee923-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee923-111">-DefaultProfile</span></span>
<span data-ttu-id="ee923-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee923-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee923-113">-Location</span><span class="sxs-lookup"><span data-stu-id="ee923-113">-Location</span></span>
<span data-ttu-id="ee923-114">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="ee923-114">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee923-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee923-115">-SubscriptionId</span></span>
<span data-ttu-id="ee923-116">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ee923-116">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee923-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee923-117">CommonParameters</span></span>
<span data-ttu-id="ee923-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee923-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee923-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee923-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee923-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee923-120">INPUTS</span></span>

## <span data-ttu-id="ee923-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee923-121">OUTPUTS</span></span>

### <span data-ttu-id="ee923-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="ee923-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="ee923-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee923-123">NOTES</span></span>

<span data-ttu-id="ee923-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ee923-124">ALIASES</span></span>

## <span data-ttu-id="ee923-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee923-125">RELATED LINKS</span></span>

