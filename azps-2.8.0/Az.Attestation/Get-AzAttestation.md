---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727884"
---
# <span data-ttu-id="a0b65-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="a0b65-101">Get-AzAttestation</span></span>

## <span data-ttu-id="a0b65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0b65-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b65-103">Получает аттестацию.</span><span class="sxs-lookup"><span data-stu-id="a0b65-103">Gets an attestation.</span></span>

## <span data-ttu-id="a0b65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0b65-104">SYNTAX</span></span>

### <span data-ttu-id="a0b65-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0b65-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0b65-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0b65-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b65-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0b65-107">DESCRIPTION</span></span>
<span data-ttu-id="a0b65-108">Командлет Get-AzAttestation получает сведения о аттестации в подписке.</span><span class="sxs-lookup"><span data-stu-id="a0b65-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="a0b65-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0b65-109">EXAMPLES</span></span>

### <span data-ttu-id="a0b65-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a0b65-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="a0b65-111">Получение подтверждения "пример" в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="a0b65-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="a0b65-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0b65-112">PARAMETERS</span></span>

### <span data-ttu-id="a0b65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b65-113">-DefaultProfile</span></span>
<span data-ttu-id="a0b65-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0b65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0b65-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a0b65-115">-Name</span></span>
<span data-ttu-id="a0b65-116">Имя аттестации.</span><span class="sxs-lookup"><span data-stu-id="a0b65-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b65-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b65-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0b65-118">Указывает имя группы ресурсов, связанной с запрашиваемой аттестацией.</span><span class="sxs-lookup"><span data-stu-id="a0b65-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b65-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0b65-119">-ResourceId</span></span>
<span data-ttu-id="a0b65-120">Указывает имя ResourceID, связанного с запрашиваемой аттестацией</span><span class="sxs-lookup"><span data-stu-id="a0b65-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b65-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b65-121">CommonParameters</span></span>
<span data-ttu-id="a0b65-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0b65-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b65-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0b65-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b65-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0b65-124">INPUTS</span></span>

### <span data-ttu-id="a0b65-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b65-125">System.String</span></span>

## <span data-ttu-id="a0b65-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0b65-126">OUTPUTS</span></span>

### <span data-ttu-id="a0b65-127">Microsoft. Azure. Commands. аттестация. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="a0b65-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="a0b65-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0b65-128">NOTES</span></span>

## <span data-ttu-id="a0b65-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0b65-129">RELATED LINKS</span></span>
