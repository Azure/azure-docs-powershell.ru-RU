---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965219"
---
# <span data-ttu-id="22815-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="22815-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="22815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22815-102">SYNOPSIS</span></span>
<span data-ttu-id="22815-103">Удаляет проверку.</span><span class="sxs-lookup"><span data-stu-id="22815-103">Deletes an attestation.</span></span>

## <span data-ttu-id="22815-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22815-104">SYNTAX</span></span>

### <span data-ttu-id="22815-105">ByAvailableAttestation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22815-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22815-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="22815-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22815-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="22815-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22815-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22815-108">DESCRIPTION</span></span>
<span data-ttu-id="22815-109">Указанный Remove-AzAttestation для этой проверки удаляется.</span><span class="sxs-lookup"><span data-stu-id="22815-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="22815-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22815-110">EXAMPLES</span></span>

### <span data-ttu-id="22815-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22815-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="22815-112">Удалите поставщика услуг attestation с именем *pshtest3* в группе ресурсов *psh-test-rg* из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="22815-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="22815-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22815-113">PARAMETERS</span></span>

### <span data-ttu-id="22815-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22815-114">-DefaultProfile</span></span>
<span data-ttu-id="22815-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22815-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22815-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22815-116">-InputObject</span></span>
<span data-ttu-id="22815-117">Объект attestation, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="22815-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22815-118">-Name</span><span class="sxs-lookup"><span data-stu-id="22815-118">-Name</span></span>
<span data-ttu-id="22815-119">Указывает имя удаляемой проверки.</span><span class="sxs-lookup"><span data-stu-id="22815-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22815-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22815-120">-PassThru</span></span>
<span data-ttu-id="22815-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22815-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="22815-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="22815-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="22815-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22815-123">-ResourceGroupName</span></span>
<span data-ttu-id="22815-124">Указывает имя группы ресурсов для azure, во время проверки которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="22815-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22815-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22815-125">-ResourceId</span></span>
<span data-ttu-id="22815-126">ИД ресурса attestation.</span><span class="sxs-lookup"><span data-stu-id="22815-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22815-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22815-127">-Confirm</span></span>
<span data-ttu-id="22815-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="22815-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22815-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22815-129">-WhatIf</span></span>
<span data-ttu-id="22815-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22815-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22815-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22815-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22815-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22815-132">CommonParameters</span></span>
<span data-ttu-id="22815-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22815-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22815-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22815-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22815-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22815-135">INPUTS</span></span>

### <span data-ttu-id="22815-136">System.String</span><span class="sxs-lookup"><span data-stu-id="22815-136">System.String</span></span>

### <span data-ttu-id="22815-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="22815-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="22815-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22815-138">OUTPUTS</span></span>

### <span data-ttu-id="22815-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22815-139">System.Boolean</span></span>

## <span data-ttu-id="22815-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22815-140">NOTES</span></span>

## <span data-ttu-id="22815-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22815-141">RELATED LINKS</span></span>
