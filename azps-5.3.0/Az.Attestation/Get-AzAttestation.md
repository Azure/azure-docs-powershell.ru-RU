---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422876"
---
# <span data-ttu-id="84987-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="84987-101">Get-AzAttestation</span></span>

## <span data-ttu-id="84987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84987-102">SYNOPSIS</span></span>
<span data-ttu-id="84987-103">Возвращает проверку.</span><span class="sxs-lookup"><span data-stu-id="84987-103">Gets an attestation.</span></span>

## <span data-ttu-id="84987-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84987-104">SYNTAX</span></span>

### <span data-ttu-id="84987-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84987-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84987-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84987-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84987-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="84987-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84987-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84987-108">DESCRIPTION</span></span>
<span data-ttu-id="84987-109">С Get-AzAttestation- и более подробной информации о проверке, которая возвращается в подписку.</span><span class="sxs-lookup"><span data-stu-id="84987-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="84987-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84987-110">EXAMPLES</span></span>

### <span data-ttu-id="84987-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84987-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="84987-112">Получить pshtestation Provider *pshtest* в группе *ресурсов psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="84987-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="84987-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="84987-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="84987-114">Получить все доступные поставщики услуг attestation по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84987-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="84987-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="84987-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="84987-116">Получить поставщика по умолчанию для проверки attestation из расположения *"Восток. США 2"*</span><span class="sxs-lookup"><span data-stu-id="84987-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="84987-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84987-117">PARAMETERS</span></span>

### <span data-ttu-id="84987-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84987-118">-DefaultProfile</span></span>
<span data-ttu-id="84987-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84987-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84987-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="84987-120">-DefaultProvider</span></span>
<span data-ttu-id="84987-121">Указывает, что это запрос к поставщику услуг проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84987-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84987-122">-Location</span><span class="sxs-lookup"><span data-stu-id="84987-122">-Location</span></span>
<span data-ttu-id="84987-123">Определяет расположение поставщика для проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84987-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84987-124">-Name</span><span class="sxs-lookup"><span data-stu-id="84987-124">-Name</span></span>
<span data-ttu-id="84987-125">Название проверки.</span><span class="sxs-lookup"><span data-stu-id="84987-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84987-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84987-126">-ResourceGroupName</span></span>
<span data-ttu-id="84987-127">Имя группы ресурсов, связанной с запрашиваемой проверкой.</span><span class="sxs-lookup"><span data-stu-id="84987-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84987-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84987-128">-ResourceId</span></span>
<span data-ttu-id="84987-129">Указывает имя ИД ресурса, связанного с запрашиваемой проверкой при проверке.</span><span class="sxs-lookup"><span data-stu-id="84987-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84987-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84987-130">CommonParameters</span></span>
<span data-ttu-id="84987-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84987-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84987-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84987-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84987-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84987-133">INPUTS</span></span>

### <span data-ttu-id="84987-134">System.String</span><span class="sxs-lookup"><span data-stu-id="84987-134">System.String</span></span>

## <span data-ttu-id="84987-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84987-135">OUTPUTS</span></span>

### <span data-ttu-id="84987-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="84987-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="84987-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84987-137">NOTES</span></span>

## <span data-ttu-id="84987-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84987-138">RELATED LINKS</span></span>
