---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406639"
---
# <span data-ttu-id="4bb62-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="4bb62-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="4bb62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb62-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb62-103">Задает политику для клиента в Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="4bb62-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="4bb62-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4bb62-104">SYNTAX</span></span>

### <span data-ttu-id="4bb62-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bb62-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bb62-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bb62-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bb62-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb62-107">DESCRIPTION</span></span>
<span data-ttu-id="4bb62-108">С Set-AzAttestationPolicy настраивает политику клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="4bb62-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="4bb62-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4bb62-109">EXAMPLES</span></span>

### <span data-ttu-id="4bb62-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4bb62-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="4bb62-111">Задает определяемую пользователем политику для типа *TEE SgxEnclave* для поставщика *attestation с* помощью формата текстовой политики (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4bb62-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="4bb62-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4bb62-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="4bb62-113">Задает определяемую пользователем политику для типа *TEE типа SgxEnclave* для поставщика attestation Provider *pshtest* с использованием формата политики JWT.</span><span class="sxs-lookup"><span data-stu-id="4bb62-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="4bb62-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb62-114">PARAMETERS</span></span>

### <span data-ttu-id="4bb62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb62-115">-DefaultProfile</span></span>
<span data-ttu-id="4bb62-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb62-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4bb62-117">-Name</span></span>
<span data-ttu-id="4bb62-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="4bb62-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="4bb62-119">Этот cmdlet задает политику проверки для клиента, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4bb62-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bb62-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4bb62-120">-PassThru</span></span>
<span data-ttu-id="4bb62-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4bb62-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4bb62-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="4bb62-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4bb62-123">-Политика</span><span class="sxs-lookup"><span data-stu-id="4bb62-123">-Policy</span></span>
<span data-ttu-id="4bb62-124">Определяет заданный документ политики.</span><span class="sxs-lookup"><span data-stu-id="4bb62-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="4bb62-125">Формат политики может быть текстовым или веб-токеном JSON (JWT).</span><span class="sxs-lookup"><span data-stu-id="4bb62-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="4bb62-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="4bb62-126">-PolicyFormat</span></span>
<span data-ttu-id="4bb62-127">Формат политики (текстовый или JWT-маркер JSON).</span><span class="sxs-lookup"><span data-stu-id="4bb62-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="4bb62-128">По умолчанию политика имеет текстовый формат.</span><span class="sxs-lookup"><span data-stu-id="4bb62-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="4bb62-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb62-129">-ResourceGroupName</span></span>
<span data-ttu-id="4bb62-130">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="4bb62-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="4bb62-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bb62-131">-ResourceId</span></span>
<span data-ttu-id="4bb62-132">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="4bb62-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="4bb62-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="4bb62-133">-Tee</span></span>
<span data-ttu-id="4bb62-134">Тип доверенного типа среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="4bb62-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="4bb62-135">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="4bb62-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="4bb62-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bb62-136">-Confirm</span></span>
<span data-ttu-id="4bb62-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4bb62-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bb62-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb62-138">-WhatIf</span></span>
<span data-ttu-id="4bb62-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb62-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bb62-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4bb62-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bb62-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb62-141">CommonParameters</span></span>
<span data-ttu-id="4bb62-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb62-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb62-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bb62-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb62-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb62-144">INPUTS</span></span>

### <span data-ttu-id="4bb62-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb62-145">System.String</span></span>

## <span data-ttu-id="4bb62-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb62-146">OUTPUTS</span></span>

### <span data-ttu-id="4bb62-147">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb62-147">System.String</span></span>

## <span data-ttu-id="4bb62-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4bb62-148">NOTES</span></span>

## <span data-ttu-id="4bb62-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bb62-149">RELATED LINKS</span></span>
