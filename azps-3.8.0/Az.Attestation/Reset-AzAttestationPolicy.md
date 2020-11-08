---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072726"
---
# <span data-ttu-id="0451a-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="0451a-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="0451a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0451a-102">SYNOPSIS</span></span>
<span data-ttu-id="0451a-103">Сброс политики клиента в Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="0451a-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="0451a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0451a-104">SYNTAX</span></span>

### <span data-ttu-id="0451a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0451a-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0451a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0451a-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0451a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0451a-107">DESCRIPTION</span></span>
<span data-ttu-id="0451a-108">Командлет Reset-AzAttestationPolicy сбрасывает определенную пользователем политику аттестации из клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="0451a-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0451a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0451a-109">EXAMPLES</span></span>

### <span data-ttu-id="0451a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0451a-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="0451a-111">Сброс политики на значение по умолчанию для поставщика аттестации *pshtest* для надежной среды выполнения типа *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="0451a-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="0451a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0451a-112">PARAMETERS</span></span>

### <span data-ttu-id="0451a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0451a-113">-DefaultProfile</span></span>
<span data-ttu-id="0451a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0451a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0451a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0451a-115">-Name</span></span>
<span data-ttu-id="0451a-116">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="0451a-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="0451a-117">Этот командлет сбрасывает политику аттестации для клиента, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0451a-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="0451a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0451a-118">-PassThru</span></span>
<span data-ttu-id="0451a-119">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0451a-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0451a-120">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="0451a-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0451a-121">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="0451a-121">-Policy</span></span>
<span data-ttu-id="0451a-122">Указывает веб-маркер JSON, описывающий документ политики для сброса.</span><span class="sxs-lookup"><span data-stu-id="0451a-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="0451a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0451a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0451a-124">Указывает имя группы ресурсов для поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="0451a-124">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="0451a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0451a-125">-ResourceId</span></span>
<span data-ttu-id="0451a-126">Указывает ResourceID поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="0451a-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="0451a-127">-Надежной среды выполнения</span><span class="sxs-lookup"><span data-stu-id="0451a-127">-Tee</span></span>
<span data-ttu-id="0451a-128">Указывает тип надежной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="0451a-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="0451a-129">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="0451a-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="0451a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0451a-130">-Confirm</span></span>
<span data-ttu-id="0451a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0451a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0451a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0451a-132">-WhatIf</span></span>
<span data-ttu-id="0451a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0451a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0451a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0451a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0451a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0451a-135">CommonParameters</span></span>
<span data-ttu-id="0451a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0451a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0451a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0451a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0451a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0451a-138">INPUTS</span></span>

### <span data-ttu-id="0451a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0451a-139">System.String</span></span>

## <span data-ttu-id="0451a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0451a-140">OUTPUTS</span></span>

### <span data-ttu-id="0451a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0451a-141">System.Boolean</span></span>

## <span data-ttu-id="0451a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="0451a-142">NOTES</span></span>

## <span data-ttu-id="0451a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0451a-143">RELATED LINKS</span></span>
