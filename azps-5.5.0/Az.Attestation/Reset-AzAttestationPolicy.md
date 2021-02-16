---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235305"
---
# <span data-ttu-id="1c147-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="1c147-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="1c147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c147-102">SYNOPSIS</span></span>
<span data-ttu-id="1c147-103">Сбрасывает политику клиента в Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="1c147-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="1c147-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c147-104">SYNTAX</span></span>

### <span data-ttu-id="1c147-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c147-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c147-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c147-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c147-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c147-107">DESCRIPTION</span></span>
<span data-ttu-id="1c147-108">Этот Reset-AzAttestationPolicy сбрасывает политику проверки, задатую пользователем, для клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="1c147-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="1c147-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c147-109">EXAMPLES</span></span>

### <span data-ttu-id="1c147-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c147-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="1c147-111">Сброс политики по умолчанию для поставщика attestation Provider *pshtest* для Tee type *SgxEnclave.*</span><span class="sxs-lookup"><span data-stu-id="1c147-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="1c147-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1c147-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="1c147-113">Если pshtest provider имеет значение *pshtest,* настроенное для использования модели изолированного доверия, сбросьйте значение политики по умолчанию для *типа Tee SgxEnclave,* включив политику с подписью.</span><span class="sxs-lookup"><span data-stu-id="1c147-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="1c147-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c147-114">PARAMETERS</span></span>

### <span data-ttu-id="1c147-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c147-115">-DefaultProfile</span></span>
<span data-ttu-id="1c147-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c147-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c147-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1c147-117">-Name</span></span>
<span data-ttu-id="1c147-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="1c147-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="1c147-119">Этот cmdlet сбрасывает политику проверки для клиента, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1c147-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c147-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c147-120">-PassThru</span></span>
<span data-ttu-id="1c147-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c147-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1c147-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="1c147-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1c147-123">-Политика</span><span class="sxs-lookup"><span data-stu-id="1c147-123">-Policy</span></span>
<span data-ttu-id="1c147-124">Указывает веб-токен JSON, описывающий документ политики, который нужно сбросить.</span><span class="sxs-lookup"><span data-stu-id="1c147-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="1c147-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c147-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c147-126">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="1c147-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="1c147-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c147-127">-ResourceId</span></span>
<span data-ttu-id="1c147-128">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="1c147-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="1c147-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="1c147-129">-Tee</span></span>
<span data-ttu-id="1c147-130">Тип доверенного типа среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="1c147-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="1c147-131">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="1c147-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="1c147-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c147-132">-Confirm</span></span>
<span data-ttu-id="1c147-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c147-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c147-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c147-134">-WhatIf</span></span>
<span data-ttu-id="1c147-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c147-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c147-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c147-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c147-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c147-137">CommonParameters</span></span>
<span data-ttu-id="1c147-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c147-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c147-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c147-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c147-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c147-140">INPUTS</span></span>

### <span data-ttu-id="1c147-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1c147-141">System.String</span></span>

## <span data-ttu-id="1c147-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c147-142">OUTPUTS</span></span>

### <span data-ttu-id="1c147-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c147-143">System.Boolean</span></span>

## <span data-ttu-id="1c147-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c147-144">NOTES</span></span>

## <span data-ttu-id="1c147-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c147-145">RELATED LINKS</span></span>
