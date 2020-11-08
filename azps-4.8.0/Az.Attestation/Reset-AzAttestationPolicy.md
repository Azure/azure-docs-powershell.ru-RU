---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235113"
---
# <span data-ttu-id="cd5db-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="cd5db-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="cd5db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd5db-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5db-103">Сброс политики клиента в Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="cd5db-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="cd5db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd5db-104">SYNTAX</span></span>

### <span data-ttu-id="cd5db-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd5db-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd5db-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd5db-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd5db-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd5db-107">DESCRIPTION</span></span>
<span data-ttu-id="cd5db-108">Командлет Reset-AzAttestationPolicy сбрасывает определенную пользователем политику аттестации из клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5db-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="cd5db-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd5db-109">EXAMPLES</span></span>

### <span data-ttu-id="cd5db-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd5db-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="cd5db-111">Сброс политики на значение по умолчанию для поставщика аттестации *pshtest* для надежной среды выполнения типа *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="cd5db-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="cd5db-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cd5db-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="cd5db-113">Если поставщик аттестации *pshtest* настроен на использование модели изолированного доверия, установите для параметра политики значение по умолчанию для надежной среды выполнения Type *SgxEnclave* , включив подписанную политику.</span><span class="sxs-lookup"><span data-stu-id="cd5db-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="cd5db-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd5db-114">PARAMETERS</span></span>

### <span data-ttu-id="cd5db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5db-115">-DefaultProfile</span></span>
<span data-ttu-id="cd5db-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5db-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd5db-117">-Name</span></span>
<span data-ttu-id="cd5db-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="cd5db-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="cd5db-119">Этот командлет сбрасывает политику аттестации для клиента, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="cd5db-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd5db-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd5db-120">-PassThru</span></span>
<span data-ttu-id="cd5db-121">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd5db-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cd5db-122">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="cd5db-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cd5db-123">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="cd5db-123">-Policy</span></span>
<span data-ttu-id="cd5db-124">Указывает веб-маркер JSON, описывающий документ политики для сброса.</span><span class="sxs-lookup"><span data-stu-id="cd5db-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="cd5db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5db-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd5db-126">Указывает имя группы ресурсов для поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="cd5db-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="cd5db-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd5db-127">-ResourceId</span></span>
<span data-ttu-id="cd5db-128">Указывает ResourceID поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="cd5db-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="cd5db-129">-Надежной среды выполнения</span><span class="sxs-lookup"><span data-stu-id="cd5db-129">-Tee</span></span>
<span data-ttu-id="cd5db-130">Указывает тип надежной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd5db-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="cd5db-131">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="cd5db-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="cd5db-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd5db-132">-Confirm</span></span>
<span data-ttu-id="cd5db-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd5db-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd5db-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd5db-134">-WhatIf</span></span>
<span data-ttu-id="cd5db-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd5db-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd5db-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd5db-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd5db-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5db-137">CommonParameters</span></span>
<span data-ttu-id="cd5db-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd5db-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5db-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd5db-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5db-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd5db-140">INPUTS</span></span>

### <span data-ttu-id="cd5db-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cd5db-141">System.String</span></span>

## <span data-ttu-id="cd5db-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd5db-142">OUTPUTS</span></span>

### <span data-ttu-id="cd5db-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd5db-143">System.Boolean</span></span>

## <span data-ttu-id="cd5db-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd5db-144">NOTES</span></span>

## <span data-ttu-id="cd5db-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd5db-145">RELATED LINKS</span></span>
