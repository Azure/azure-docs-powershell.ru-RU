---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562648"
---
# <span data-ttu-id="e56e8-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e56e8-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="e56e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e56e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e56e8-103">Получение решений для системы безопасности, обнаруженных центром безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="e56e8-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e56e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e56e8-104">SYNTAX</span></span>

### <span data-ttu-id="e56e8-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e56e8-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56e8-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e56e8-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e56e8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e56e8-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e56e8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e56e8-108">DESCRIPTION</span></span>
<span data-ttu-id="e56e8-109">Решения для обеспечения безопасности автоматически определяются центром безопасности Azure, используйте этот командлет для просмотра обнаруженных решений для обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="e56e8-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="e56e8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e56e8-110">EXAMPLES</span></span>

### <span data-ttu-id="e56e8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e56e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="e56e8-112">Получение всех обнаруженных решений безопасности в подписке</span><span class="sxs-lookup"><span data-stu-id="e56e8-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="e56e8-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e56e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="e56e8-114">Получение определенного решения для системы безопасности</span><span class="sxs-lookup"><span data-stu-id="e56e8-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="e56e8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e56e8-115">PARAMETERS</span></span>

### <span data-ttu-id="e56e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56e8-116">-DefaultProfile</span></span>
<span data-ttu-id="e56e8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e56e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56e8-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e56e8-118">-Location</span></span>
<span data-ttu-id="e56e8-119">Поиска.</span><span class="sxs-lookup"><span data-stu-id="e56e8-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56e8-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e56e8-120">-Name</span></span>
<span data-ttu-id="e56e8-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e56e8-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e56e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="e56e8-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e56e8-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56e8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e56e8-124">-ResourceId</span></span>
<span data-ttu-id="e56e8-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e56e8-125">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56e8-126">CommonParameters</span></span>
<span data-ttu-id="e56e8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e56e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56e8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e56e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56e8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e56e8-129">INPUTS</span></span>

### <span data-ttu-id="e56e8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e56e8-130">System.String</span></span>

## <span data-ttu-id="e56e8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e56e8-131">OUTPUTS</span></span>

### <span data-ttu-id="e56e8-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e56e8-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="e56e8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e56e8-133">NOTES</span></span>

## <span data-ttu-id="e56e8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e56e8-134">RELATED LINKS</span></span>
