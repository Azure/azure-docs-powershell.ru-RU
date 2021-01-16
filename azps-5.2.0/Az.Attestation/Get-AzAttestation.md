---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406695"
---
# <span data-ttu-id="32022-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="32022-101">Get-AzAttestation</span></span>

## <span data-ttu-id="32022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32022-102">SYNOPSIS</span></span>
<span data-ttu-id="32022-103">Возвращает проверку.</span><span class="sxs-lookup"><span data-stu-id="32022-103">Gets an attestation.</span></span>

## <span data-ttu-id="32022-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32022-104">SYNTAX</span></span>

### <span data-ttu-id="32022-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32022-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32022-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32022-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32022-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="32022-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32022-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32022-108">DESCRIPTION</span></span>
<span data-ttu-id="32022-109">Этот Get-AzAttestation получает сведения о тесте в подписке.</span><span class="sxs-lookup"><span data-stu-id="32022-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="32022-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32022-110">EXAMPLES</span></span>

### <span data-ttu-id="32022-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32022-111">Example 1</span></span>
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

<span data-ttu-id="32022-112">Получить Pshtestation Provider *pshtest* в группе *ресурсов psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="32022-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="32022-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32022-113">Example 2</span></span>
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

<span data-ttu-id="32022-114">Получить все доступные поставщики услуг attestation по умолчанию</span><span class="sxs-lookup"><span data-stu-id="32022-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="32022-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="32022-115">Example 3</span></span>
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

<span data-ttu-id="32022-116">Получить проверку по умолчанию для поставщика из расположения *"Восток. США 2"*</span><span class="sxs-lookup"><span data-stu-id="32022-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="32022-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32022-117">PARAMETERS</span></span>

### <span data-ttu-id="32022-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32022-118">-DefaultProfile</span></span>
<span data-ttu-id="32022-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32022-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32022-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="32022-120">-DefaultProvider</span></span>
<span data-ttu-id="32022-121">Указывает, что это запрос к поставщику проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32022-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="32022-122">-Location</span><span class="sxs-lookup"><span data-stu-id="32022-122">-Location</span></span>
<span data-ttu-id="32022-123">Определяет расположение поставщика для проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32022-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="32022-124">-Name</span><span class="sxs-lookup"><span data-stu-id="32022-124">-Name</span></span>
<span data-ttu-id="32022-125">Название проверки.</span><span class="sxs-lookup"><span data-stu-id="32022-125">Attestation Name.</span></span>

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

### <span data-ttu-id="32022-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32022-126">-ResourceGroupName</span></span>
<span data-ttu-id="32022-127">Имя группы ресурсов, связанной с запрашиваемой проверкой.</span><span class="sxs-lookup"><span data-stu-id="32022-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="32022-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32022-128">-ResourceId</span></span>
<span data-ttu-id="32022-129">Указывает имя ИД ресурса, связанного с запрашиваемой проверкой attestation.</span><span class="sxs-lookup"><span data-stu-id="32022-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="32022-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32022-130">CommonParameters</span></span>
<span data-ttu-id="32022-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32022-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32022-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32022-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32022-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32022-133">INPUTS</span></span>

### <span data-ttu-id="32022-134">System.String</span><span class="sxs-lookup"><span data-stu-id="32022-134">System.String</span></span>

## <span data-ttu-id="32022-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32022-135">OUTPUTS</span></span>

### <span data-ttu-id="32022-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="32022-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="32022-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32022-137">NOTES</span></span>

## <span data-ttu-id="32022-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32022-138">RELATED LINKS</span></span>
