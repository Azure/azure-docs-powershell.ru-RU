---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072740"
---
# <span data-ttu-id="d777f-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="d777f-101">Get-AzAttestation</span></span>

## <span data-ttu-id="d777f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d777f-102">SYNOPSIS</span></span>
<span data-ttu-id="d777f-103">Получает аттестацию.</span><span class="sxs-lookup"><span data-stu-id="d777f-103">Gets an attestation.</span></span>

## <span data-ttu-id="d777f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d777f-104">SYNTAX</span></span>

### <span data-ttu-id="d777f-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d777f-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d777f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d777f-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d777f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d777f-107">DESCRIPTION</span></span>
<span data-ttu-id="d777f-108">Командлет Get-AzAttestation получает сведения о аттестации в подписке.</span><span class="sxs-lookup"><span data-stu-id="d777f-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="d777f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d777f-109">EXAMPLES</span></span>

### <span data-ttu-id="d777f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d777f-110">Example 1</span></span>
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

<span data-ttu-id="d777f-111">Получение поставщика аттестации *pshtest* в группе ресурсов *PSH-Test-RG*.</span><span class="sxs-lookup"><span data-stu-id="d777f-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="d777f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d777f-112">PARAMETERS</span></span>

### <span data-ttu-id="d777f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d777f-113">-DefaultProfile</span></span>
<span data-ttu-id="d777f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d777f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d777f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d777f-115">-Name</span></span>
<span data-ttu-id="d777f-116">Имя аттестации.</span><span class="sxs-lookup"><span data-stu-id="d777f-116">Attestation Name.</span></span>

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

### <span data-ttu-id="d777f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d777f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d777f-118">Указывает имя группы ресурсов, связанной с запрашиваемой аттестацией.</span><span class="sxs-lookup"><span data-stu-id="d777f-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="d777f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d777f-119">-ResourceId</span></span>
<span data-ttu-id="d777f-120">Указывает имя ResourceID, связанного с запрашиваемой аттестацией</span><span class="sxs-lookup"><span data-stu-id="d777f-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="d777f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d777f-121">CommonParameters</span></span>
<span data-ttu-id="d777f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d777f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d777f-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d777f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d777f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d777f-124">INPUTS</span></span>

### <span data-ttu-id="d777f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d777f-125">System.String</span></span>

## <span data-ttu-id="d777f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d777f-126">OUTPUTS</span></span>

### <span data-ttu-id="d777f-127">Microsoft. Azure. Commands. аттестация. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="d777f-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="d777f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d777f-128">NOTES</span></span>

## <span data-ttu-id="d777f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d777f-129">RELATED LINKS</span></span>
