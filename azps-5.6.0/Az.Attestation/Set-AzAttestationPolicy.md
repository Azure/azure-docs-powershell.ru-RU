---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c32a9e2fd474578c8526c8352e8649cb84d8b016
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966787"
---
# <span data-ttu-id="1455d-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="1455d-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="1455d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1455d-102">SYNOPSIS</span></span>
<span data-ttu-id="1455d-103">Задает политику для клиента в Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="1455d-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="1455d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1455d-104">SYNTAX</span></span>

### <span data-ttu-id="1455d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1455d-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1455d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1455d-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1455d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1455d-107">DESCRIPTION</span></span>
<span data-ttu-id="1455d-108">С Set-AzAttestationPolicy настраивает политику клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="1455d-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="1455d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1455d-109">EXAMPLES</span></span>

### <span data-ttu-id="1455d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1455d-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="1455d-111">Задает определяемую пользователем политику для типа *TEE типа SgxEnclave* для поставщика услуг attestation *pshtest* с использованием формата текстовой политики (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1455d-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="1455d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1455d-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="1455d-113">Задает определяемую пользователем политику для TEE типа *SgxEnclave* для поставщика attestation Provider *pshtest* с использованием формата политики JWT.</span><span class="sxs-lookup"><span data-stu-id="1455d-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="1455d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1455d-114">PARAMETERS</span></span>

### <span data-ttu-id="1455d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1455d-115">-DefaultProfile</span></span>
<span data-ttu-id="1455d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1455d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1455d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1455d-117">-Name</span></span>
<span data-ttu-id="1455d-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1455d-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="1455d-119">Этот cmdlet задает политику проверки для клиента, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1455d-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="1455d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1455d-120">-PassThru</span></span>
<span data-ttu-id="1455d-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1455d-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1455d-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="1455d-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1455d-123">-Политика</span><span class="sxs-lookup"><span data-stu-id="1455d-123">-Policy</span></span>
<span data-ttu-id="1455d-124">Определяет заданный документ политики.</span><span class="sxs-lookup"><span data-stu-id="1455d-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="1455d-125">Формат политики может быть текстовым или веб-токеном JSON (JWT).</span><span class="sxs-lookup"><span data-stu-id="1455d-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="1455d-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="1455d-126">-PolicyFormat</span></span>
<span data-ttu-id="1455d-127">Формат политики (текстовый или JWT-маркер JSON).</span><span class="sxs-lookup"><span data-stu-id="1455d-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="1455d-128">По умолчанию политика имеет текстовый формат.</span><span class="sxs-lookup"><span data-stu-id="1455d-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="1455d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1455d-129">-ResourceGroupName</span></span>
<span data-ttu-id="1455d-130">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="1455d-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="1455d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1455d-131">-ResourceId</span></span>
<span data-ttu-id="1455d-132">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="1455d-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="1455d-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="1455d-133">-Tee</span></span>
<span data-ttu-id="1455d-134">Тип доверенного типа среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="1455d-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="1455d-135">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="1455d-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="1455d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1455d-136">-Confirm</span></span>
<span data-ttu-id="1455d-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1455d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1455d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1455d-138">-WhatIf</span></span>
<span data-ttu-id="1455d-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1455d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1455d-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1455d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1455d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1455d-141">CommonParameters</span></span>
<span data-ttu-id="1455d-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1455d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1455d-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1455d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1455d-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1455d-144">INPUTS</span></span>

### <span data-ttu-id="1455d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1455d-145">System.String</span></span>

## <span data-ttu-id="1455d-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1455d-146">OUTPUTS</span></span>

### <span data-ttu-id="1455d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1455d-147">System.String</span></span>

## <span data-ttu-id="1455d-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1455d-148">NOTES</span></span>

## <span data-ttu-id="1455d-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1455d-149">RELATED LINKS</span></span>
