---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: b628d93d44b863b4af05f09dd4d132ec986702e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966792"
---
# <span data-ttu-id="94c78-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="94c78-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="94c78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c78-102">SYNOPSIS</span></span>
<span data-ttu-id="94c78-103">Сбрасывает политику клиента в Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="94c78-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="94c78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94c78-104">SYNTAX</span></span>

### <span data-ttu-id="94c78-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="94c78-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c78-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94c78-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94c78-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94c78-107">DESCRIPTION</span></span>
<span data-ttu-id="94c78-108">Этот Reset-AzAttestationPolicy сбрасывает политику проверки, задатую пользователем, для клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="94c78-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="94c78-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94c78-109">EXAMPLES</span></span>

### <span data-ttu-id="94c78-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94c78-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="94c78-111">Сброс политики по умолчанию для поставщика attestation Provider *pshtest* для Tee type *SgxEnclave.*</span><span class="sxs-lookup"><span data-stu-id="94c78-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="94c78-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94c78-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="94c78-113">Если pshtest provider имеет значение *pshtest,* настроенное для использования модели изолированного доверия, сбросьйте значение политики по умолчанию для *типа Tee SgxEnclave,* включив политику с подписью.</span><span class="sxs-lookup"><span data-stu-id="94c78-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="94c78-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94c78-114">PARAMETERS</span></span>

### <span data-ttu-id="94c78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c78-115">-DefaultProfile</span></span>
<span data-ttu-id="94c78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94c78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c78-117">-Name</span><span class="sxs-lookup"><span data-stu-id="94c78-117">-Name</span></span>
<span data-ttu-id="94c78-118">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="94c78-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="94c78-119">Этот cmdlet сбрасывает политику проверки для клиента, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="94c78-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="94c78-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94c78-120">-PassThru</span></span>
<span data-ttu-id="94c78-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94c78-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="94c78-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="94c78-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="94c78-123">-Политика</span><span class="sxs-lookup"><span data-stu-id="94c78-123">-Policy</span></span>
<span data-ttu-id="94c78-124">Указывает веб-токен JSON, описывающий документ политики, который нужно сбросить.</span><span class="sxs-lookup"><span data-stu-id="94c78-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="94c78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c78-125">-ResourceGroupName</span></span>
<span data-ttu-id="94c78-126">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="94c78-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="94c78-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94c78-127">-ResourceId</span></span>
<span data-ttu-id="94c78-128">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="94c78-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="94c78-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="94c78-129">-Tee</span></span>
<span data-ttu-id="94c78-130">Тип доверенного типа среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="94c78-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="94c78-131">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="94c78-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="94c78-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94c78-132">-Confirm</span></span>
<span data-ttu-id="94c78-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c78-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c78-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c78-134">-WhatIf</span></span>
<span data-ttu-id="94c78-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c78-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c78-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94c78-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c78-137">CommonParameters</span></span>
<span data-ttu-id="94c78-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c78-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94c78-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c78-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94c78-140">INPUTS</span></span>

### <span data-ttu-id="94c78-141">System.String</span><span class="sxs-lookup"><span data-stu-id="94c78-141">System.String</span></span>

## <span data-ttu-id="94c78-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94c78-142">OUTPUTS</span></span>

### <span data-ttu-id="94c78-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94c78-143">System.Boolean</span></span>

## <span data-ttu-id="94c78-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94c78-144">NOTES</span></span>

## <span data-ttu-id="94c78-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94c78-145">RELATED LINKS</span></span>
