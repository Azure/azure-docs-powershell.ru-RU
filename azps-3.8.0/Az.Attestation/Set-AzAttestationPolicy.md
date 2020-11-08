---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072725"
---
# <span data-ttu-id="2a2bb-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="2a2bb-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="2a2bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2bb-103">Задает политику клиента в Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="2a2bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a2bb-104">SYNTAX</span></span>

### <span data-ttu-id="2a2bb-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a2bb-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2bb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a2bb-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a2bb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a2bb-107">DESCRIPTION</span></span>
<span data-ttu-id="2a2bb-108">Командлет Set-AzAttestationPolicy задает политику из клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="2a2bb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a2bb-109">EXAMPLES</span></span>

### <span data-ttu-id="2a2bb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a2bb-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="2a2bb-111">Задает политику, определенную пользователем, для надежной среды выполнения типа *SgxEnclave* для поставщика аттестации *pshtest* с помощью формата текстовой политики (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="2a2bb-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="2a2bb-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2a2bb-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="2a2bb-113">Задает политику, определенную пользователем, для надежной среды выполнения типа *SgxEnclave* для поставщика аттестации *pshtest* с помощью формата политики JWT.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="2a2bb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a2bb-114">PARAMETERS</span></span>

### <span data-ttu-id="2a2bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2bb-115">-DefaultProfile</span></span>
<span data-ttu-id="2a2bb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2bb-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a2bb-117">-Name</span></span>
<span data-ttu-id="2a2bb-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="2a2bb-119">Этот командлет задает политику аттестации для клиента, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a2bb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a2bb-120">-PassThru</span></span>
<span data-ttu-id="2a2bb-121">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2a2bb-122">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2bb-123">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="2a2bb-123">-Policy</span></span>
<span data-ttu-id="2a2bb-124">Указывает документ политики, который нужно задать.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="2a2bb-125">Формат политики может быть как текстом, так и веб-токеном JSON (JWT).</span><span class="sxs-lookup"><span data-stu-id="2a2bb-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="2a2bb-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="2a2bb-126">-PolicyFormat</span></span>
<span data-ttu-id="2a2bb-127">Задает формат для политики: Text или JWT (веб-маркер JSON).</span><span class="sxs-lookup"><span data-stu-id="2a2bb-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="2a2bb-128">Формат политики по умолчанию — текст.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-128">The default policy format is Text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2bb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2bb-129">-ResourceGroupName</span></span>
<span data-ttu-id="2a2bb-130">Указывает имя группы ресурсов для поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="2a2bb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a2bb-131">-ResourceId</span></span>
<span data-ttu-id="2a2bb-132">Указывает ResourceID поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="2a2bb-133">-Надежной среды выполнения</span><span class="sxs-lookup"><span data-stu-id="2a2bb-133">-Tee</span></span>
<span data-ttu-id="2a2bb-134">Указывает тип надежной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="2a2bb-135">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="2a2bb-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a2bb-136">-Confirm</span></span>
<span data-ttu-id="2a2bb-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2bb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2bb-138">-WhatIf</span></span>
<span data-ttu-id="2a2bb-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a2bb-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2bb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2bb-141">CommonParameters</span></span>
<span data-ttu-id="2a2bb-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2bb-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a2bb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2bb-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a2bb-144">INPUTS</span></span>

### <span data-ttu-id="2a2bb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2bb-145">System.String</span></span>

## <span data-ttu-id="2a2bb-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a2bb-146">OUTPUTS</span></span>

### <span data-ttu-id="2a2bb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2bb-147">System.String</span></span>

## <span data-ttu-id="2a2bb-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a2bb-148">NOTES</span></span>

## <span data-ttu-id="2a2bb-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a2bb-149">RELATED LINKS</span></span>
