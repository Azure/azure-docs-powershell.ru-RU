---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407900"
---
# <span data-ttu-id="2bb34-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="2bb34-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="2bb34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bb34-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb34-103">Регулируемые стандарты соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="2bb34-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="2bb34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2bb34-104">SYNTAX</span></span>

### <span data-ttu-id="2bb34-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2bb34-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb34-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2bb34-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bb34-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bb34-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bb34-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bb34-108">DESCRIPTION</span></span>
<span data-ttu-id="2bb34-109">Получите определенные сведения о соответствии нормативным требованиям или со списком всех нормативных стандартов в рамках определенной подписки.</span><span class="sxs-lookup"><span data-stu-id="2bb34-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="2bb34-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2bb34-110">EXAMPLES</span></span>

### <span data-ttu-id="2bb34-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bb34-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2bb34-112">Получите все нормативные стандарты в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="2bb34-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="2bb34-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2bb34-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2bb34-114">Получите сведения об определенных нормативных стандартах в соответствии со стандартным именем.</span><span class="sxs-lookup"><span data-stu-id="2bb34-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="2bb34-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2bb34-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="2bb34-116">Получите подробные сведения об определенных нормативных требованиях в соответствии с идом ресурса.</span><span class="sxs-lookup"><span data-stu-id="2bb34-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="2bb34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bb34-117">PARAMETERS</span></span>

### <span data-ttu-id="2bb34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb34-118">-DefaultProfile</span></span>
<span data-ttu-id="2bb34-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb34-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2bb34-120">-Name</span></span>
<span data-ttu-id="2bb34-121">Стандартное имя.</span><span class="sxs-lookup"><span data-stu-id="2bb34-121">Standard name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb34-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bb34-122">-ResourceId</span></span>
<span data-ttu-id="2bb34-123">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="2bb34-123">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb34-124">CommonParameters</span></span>
<span data-ttu-id="2bb34-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb34-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bb34-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb34-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bb34-127">INPUTS</span></span>

### <span data-ttu-id="2bb34-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2bb34-128">System.String</span></span>

## <span data-ttu-id="2bb34-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2bb34-129">OUTPUTS</span></span>

### <span data-ttu-id="2bb34-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="2bb34-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="2bb34-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2bb34-131">NOTES</span></span>

## <span data-ttu-id="2bb34-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bb34-132">RELATED LINKS</span></span>
