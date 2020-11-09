---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315341"
---
# <span data-ttu-id="114b0-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="114b0-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="114b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="114b0-102">SYNOPSIS</span></span>
<span data-ttu-id="114b0-103">Сброс политики клиента в Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="114b0-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="114b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="114b0-104">SYNTAX</span></span>

### <span data-ttu-id="114b0-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="114b0-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="114b0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="114b0-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="114b0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="114b0-107">DESCRIPTION</span></span>
<span data-ttu-id="114b0-108">Командлет Reset-AzAttestationPolicy сбрасывает определенную пользователем политику аттестации из клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="114b0-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="114b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="114b0-109">EXAMPLES</span></span>

### <span data-ttu-id="114b0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="114b0-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="114b0-111">Сброс политики на значение по умолчанию для поставщика аттестации *pshtest* для надежной среды выполнения типа *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="114b0-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="114b0-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="114b0-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="114b0-113">Если поставщик аттестации *pshtest* настроен на использование модели изолированного доверия, установите для параметра политики значение по умолчанию для надежной среды выполнения Type *SgxEnclave* , включив подписанную политику.</span><span class="sxs-lookup"><span data-stu-id="114b0-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="114b0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="114b0-114">PARAMETERS</span></span>

### <span data-ttu-id="114b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114b0-115">-DefaultProfile</span></span>
<span data-ttu-id="114b0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="114b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="114b0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="114b0-117">-Name</span></span>
<span data-ttu-id="114b0-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="114b0-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="114b0-119">Этот командлет сбрасывает политику аттестации для клиента, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="114b0-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="114b0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="114b0-120">-PassThru</span></span>
<span data-ttu-id="114b0-121">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="114b0-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="114b0-122">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="114b0-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="114b0-123">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="114b0-123">-Policy</span></span>
<span data-ttu-id="114b0-124">Указывает веб-маркер JSON, описывающий документ политики для сброса.</span><span class="sxs-lookup"><span data-stu-id="114b0-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="114b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="114b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="114b0-126">Указывает имя группы ресурсов для поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="114b0-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="114b0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="114b0-127">-ResourceId</span></span>
<span data-ttu-id="114b0-128">Указывает ResourceID поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="114b0-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="114b0-129">-Надежной среды выполнения</span><span class="sxs-lookup"><span data-stu-id="114b0-129">-Tee</span></span>
<span data-ttu-id="114b0-130">Указывает тип надежной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="114b0-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="114b0-131">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="114b0-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="114b0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="114b0-132">-Confirm</span></span>
<span data-ttu-id="114b0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="114b0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114b0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="114b0-134">-WhatIf</span></span>
<span data-ttu-id="114b0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="114b0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114b0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="114b0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114b0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114b0-137">CommonParameters</span></span>
<span data-ttu-id="114b0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="114b0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114b0-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="114b0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114b0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="114b0-140">INPUTS</span></span>

### <span data-ttu-id="114b0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="114b0-141">System.String</span></span>

## <span data-ttu-id="114b0-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="114b0-142">OUTPUTS</span></span>

### <span data-ttu-id="114b0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="114b0-143">System.Boolean</span></span>

## <span data-ttu-id="114b0-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="114b0-144">NOTES</span></span>

## <span data-ttu-id="114b0-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="114b0-145">RELATED LINKS</span></span>
