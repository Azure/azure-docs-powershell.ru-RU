---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: e0b86a1cd7c3e1355cfc760fecc257b3cde87561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966808"
---
# <span data-ttu-id="dae6f-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="dae6f-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="dae6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dae6f-102">SYNOPSIS</span></span>
<span data-ttu-id="dae6f-103">Удаляет надежного подписывателя политики для клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="dae6f-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="dae6f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dae6f-104">SYNTAX</span></span>

### <span data-ttu-id="dae6f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae6f-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae6f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae6f-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae6f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dae6f-107">DESCRIPTION</span></span>
<span data-ttu-id="dae6f-108">Этот Remove-AzAttestationPolicySigner удаляет надежного подписывателя политики для клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="dae6f-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="dae6f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dae6f-109">EXAMPLES</span></span>

### <span data-ttu-id="dae6f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dae6f-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="dae6f-111">Удаление надежного подписываемго для поставщика услуг attestation с именем *pshtest.*</span><span class="sxs-lookup"><span data-stu-id="dae6f-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="dae6f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dae6f-112">PARAMETERS</span></span>

### <span data-ttu-id="dae6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae6f-113">-DefaultProfile</span></span>
<span data-ttu-id="dae6f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dae6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae6f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dae6f-115">-Name</span></span>
<span data-ttu-id="dae6f-116">Указывает имя поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="dae6f-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="dae6f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae6f-117">-ResourceGroupName</span></span>
<span data-ttu-id="dae6f-118">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="dae6f-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="dae6f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dae6f-119">-ResourceId</span></span>
<span data-ttu-id="dae6f-120">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="dae6f-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="dae6f-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="dae6f-121">-Signer</span></span>
<span data-ttu-id="dae6f-122">Указывает веб-токен JSON RFC7519, содержащий претензию maa-policyCertificate, значением которой является веб-ключ RFC7517 JSON, содержащий ключ надежного подписи, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dae6f-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="dae6f-123">Для JWT RFC7519 необходимо использовать один из существующих доверенных ключей подписи.</span><span class="sxs-lookup"><span data-stu-id="dae6f-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="dae6f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dae6f-124">-Confirm</span></span>
<span data-ttu-id="dae6f-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae6f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae6f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae6f-126">-WhatIf</span></span>
<span data-ttu-id="dae6f-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae6f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae6f-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dae6f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae6f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae6f-129">CommonParameters</span></span>
<span data-ttu-id="dae6f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae6f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae6f-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dae6f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae6f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dae6f-132">INPUTS</span></span>

### <span data-ttu-id="dae6f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dae6f-133">System.String</span></span>

## <span data-ttu-id="dae6f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dae6f-134">OUTPUTS</span></span>

### <span data-ttu-id="dae6f-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="dae6f-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="dae6f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dae6f-136">NOTES</span></span>

## <span data-ttu-id="dae6f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dae6f-137">RELATED LINKS</span></span>
