---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422892"
---
# <span data-ttu-id="31efe-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="31efe-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="31efe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31efe-102">SYNOPSIS</span></span>
<span data-ttu-id="31efe-103">Добавляет надежного подписывателя политики для клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="31efe-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="31efe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31efe-104">SYNTAX</span></span>

### <span data-ttu-id="31efe-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="31efe-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31efe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31efe-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31efe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31efe-107">DESCRIPTION</span></span>
<span data-ttu-id="31efe-108">Этот Add-AzAttestationPolicySigner добавляет в Azure Attestation надежного подписывателя политики для клиента.</span><span class="sxs-lookup"><span data-stu-id="31efe-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="31efe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31efe-109">EXAMPLES</span></span>

### <span data-ttu-id="31efe-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31efe-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="31efe-111">Добавьте надежного подписываемго для поставщика услуг atteestation с именем *pshtest.*</span><span class="sxs-lookup"><span data-stu-id="31efe-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="31efe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31efe-112">PARAMETERS</span></span>

### <span data-ttu-id="31efe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31efe-113">-DefaultProfile</span></span>
<span data-ttu-id="31efe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31efe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31efe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="31efe-115">-Name</span></span>
<span data-ttu-id="31efe-116">Указывает имя поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="31efe-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="31efe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31efe-117">-ResourceGroupName</span></span>
<span data-ttu-id="31efe-118">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="31efe-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="31efe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31efe-119">-ResourceId</span></span>
<span data-ttu-id="31efe-120">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="31efe-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="31efe-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="31efe-121">-Signer</span></span>
<span data-ttu-id="31efe-122">Определяет веб-токен JSON RFC7519, содержащий претензию maa-policyCertificate, значением которой является веб-ключ RFC7517 JSON, который содержит новый надежный ключ подписи, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="31efe-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="31efe-123">Для JWT RFC7519 необходимо использовать один из существующих доверенных ключей подписи.</span><span class="sxs-lookup"><span data-stu-id="31efe-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="31efe-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31efe-124">-Confirm</span></span>
<span data-ttu-id="31efe-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="31efe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31efe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31efe-126">-WhatIf</span></span>
<span data-ttu-id="31efe-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31efe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31efe-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31efe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31efe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31efe-129">CommonParameters</span></span>
<span data-ttu-id="31efe-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31efe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31efe-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31efe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31efe-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31efe-132">INPUTS</span></span>

### <span data-ttu-id="31efe-133">System.String</span><span class="sxs-lookup"><span data-stu-id="31efe-133">System.String</span></span>

## <span data-ttu-id="31efe-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31efe-134">OUTPUTS</span></span>

### <span data-ttu-id="31efe-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="31efe-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="31efe-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31efe-136">NOTES</span></span>

## <span data-ttu-id="31efe-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31efe-137">RELATED LINKS</span></span>
