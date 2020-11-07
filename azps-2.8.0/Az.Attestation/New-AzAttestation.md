---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727883"
---
# <span data-ttu-id="d9e7c-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="d9e7c-101">New-AzAttestation</span></span>

## <span data-ttu-id="d9e7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e7c-103">Создание аттестации</span><span class="sxs-lookup"><span data-stu-id="d9e7c-103">Creates an attestation</span></span>

## <span data-ttu-id="d9e7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9e7c-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9e7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="d9e7c-106">Командлет New-AzAttestation создает аттестацию в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="d9e7c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9e7c-107">EXAMPLES</span></span>

### <span data-ttu-id="d9e7c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9e7c-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="d9e7c-109">Создание новой аттестации "пример" в текущей подписке, группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="d9e7c-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="d9e7c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9e7c-110">PARAMETERS</span></span>

### <span data-ttu-id="d9e7c-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="d9e7c-111">-AttestationPolicy</span></span>
<span data-ttu-id="d9e7c-112">Указывает политику аттестации, переданную для создания аттестации.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e7c-113">-DefaultProfile</span></span>
<span data-ttu-id="d9e7c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9e7c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9e7c-115">-Name</span></span>
<span data-ttu-id="d9e7c-116">Указывает имя создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="d9e7c-117">Имя может представлять собой любую комбинацию букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="d9e7c-118">Имя должно начинаться и заканчиваться на букву или цифру.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="d9e7c-119">Имя должно быть универсальным уникальным.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9e7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9e7c-121">Указывает имя существующей группы ресурсов, в которой будет создана аттестация.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e7c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9e7c-122">-Confirm</span></span>
<span data-ttu-id="d9e7c-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e7c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e7c-124">-WhatIf</span></span>
<span data-ttu-id="d9e7c-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9e7c-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e7c-127">CommonParameters</span></span>
<span data-ttu-id="d9e7c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9e7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e7c-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9e7c-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e7c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9e7c-130">INPUTS</span></span>

### <span data-ttu-id="d9e7c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e7c-131">System.String</span></span>

## <span data-ttu-id="d9e7c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9e7c-132">OUTPUTS</span></span>

### <span data-ttu-id="d9e7c-133">Microsoft. Azure. Commands. аттестация. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="d9e7c-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="d9e7c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9e7c-134">NOTES</span></span>

## <span data-ttu-id="d9e7c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9e7c-135">RELATED LINKS</span></span>
