---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235116"
---
# <span data-ttu-id="47b62-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="47b62-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="47b62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47b62-102">SYNOPSIS</span></span>
<span data-ttu-id="47b62-103">Добавление подписавшего доверенной политики для клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="47b62-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="47b62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47b62-104">SYNTAX</span></span>

### <span data-ttu-id="47b62-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b62-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b62-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b62-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b62-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b62-107">DESCRIPTION</span></span>
<span data-ttu-id="47b62-108">Командлет Add-AzAttestationPolicySigner добавляет подписавшего доверенную политику для клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="47b62-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="47b62-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47b62-109">EXAMPLES</span></span>

### <span data-ttu-id="47b62-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47b62-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="47b62-111">Добавьте доверенного подписавшего для поставщика Atteestation с именем *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="47b62-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="47b62-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47b62-112">PARAMETERS</span></span>

### <span data-ttu-id="47b62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b62-113">-DefaultProfile</span></span>
<span data-ttu-id="47b62-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47b62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b62-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47b62-115">-Name</span></span>
<span data-ttu-id="47b62-116">Указывает имя поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="47b62-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b62-117">-ResourceGroupName</span></span>
<span data-ttu-id="47b62-118">Указывает имя группы ресурсов для поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="47b62-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b62-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47b62-119">-ResourceId</span></span>
<span data-ttu-id="47b62-120">Указывает ResourceID поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="47b62-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="47b62-121">-Подписавшего</span><span class="sxs-lookup"><span data-stu-id="47b62-121">-Signer</span></span>
<span data-ttu-id="47b62-122">Указывает веб-токен JSON RFC7519, содержащий утверждение "Maa-policyCertificate", значение которого является веб-ключом RFC7517 JSON, который содержит новый доверенный ключ подписи для добавления.</span><span class="sxs-lookup"><span data-stu-id="47b62-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="47b62-123">RFC7519 JWT должен быть подписан одним из существующих доверенных ключей подписывания.</span><span class="sxs-lookup"><span data-stu-id="47b62-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="47b62-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b62-124">-Confirm</span></span>
<span data-ttu-id="47b62-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47b62-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b62-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b62-126">-WhatIf</span></span>
<span data-ttu-id="47b62-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47b62-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b62-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47b62-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b62-129">CommonParameters</span></span>
<span data-ttu-id="47b62-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47b62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b62-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b62-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b62-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47b62-132">INPUTS</span></span>

### <span data-ttu-id="47b62-133">System. String</span><span class="sxs-lookup"><span data-stu-id="47b62-133">System.String</span></span>

## <span data-ttu-id="47b62-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b62-134">OUTPUTS</span></span>

### <span data-ttu-id="47b62-135">Microsoft. Azure. Commands. аттестация. Models. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="47b62-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="47b62-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="47b62-136">NOTES</span></span>

## <span data-ttu-id="47b62-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47b62-137">RELATED LINKS</span></span>
