---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315350"
---
# <span data-ttu-id="ac5f9-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="ac5f9-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="ac5f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac5f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5f9-103">Удаление аттестации.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-103">Deletes an attestation.</span></span>

## <span data-ttu-id="ac5f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac5f9-104">SYNTAX</span></span>

### <span data-ttu-id="ac5f9-105">ByAvailableAttestation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac5f9-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5f9-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="ac5f9-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5f9-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="ac5f9-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5f9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac5f9-108">DESCRIPTION</span></span>
<span data-ttu-id="ac5f9-109">Командлет Remove-AzAttestation удаляет указанную аттестацию.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="ac5f9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac5f9-110">EXAMPLES</span></span>

### <span data-ttu-id="ac5f9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac5f9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="ac5f9-112">Удалите поставщика аттестации с именем *pshtest3* в группе ресурсов с именем *PSH-Test-RG* из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="ac5f9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac5f9-113">PARAMETERS</span></span>

### <span data-ttu-id="ac5f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5f9-114">-DefaultProfile</span></span>
<span data-ttu-id="ac5f9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5f9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac5f9-116">-InputObject</span></span>
<span data-ttu-id="ac5f9-117">Объект аттестации, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="ac5f9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac5f9-118">-Name</span></span>
<span data-ttu-id="ac5f9-119">Указывает имя подтверждения для удаления.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="ac5f9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac5f9-120">-PassThru</span></span>
<span data-ttu-id="ac5f9-121">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ac5f9-122">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ac5f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac5f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac5f9-124">Указывает имя группы ресурсов для аттестации Azure, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="ac5f9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac5f9-125">-ResourceId</span></span>
<span data-ttu-id="ac5f9-126">Идентификатор ресурса аттестации.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="ac5f9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac5f9-127">-Confirm</span></span>
<span data-ttu-id="ac5f9-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5f9-129">-WhatIf</span></span>
<span data-ttu-id="ac5f9-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5f9-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5f9-132">CommonParameters</span></span>
<span data-ttu-id="ac5f9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac5f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5f9-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac5f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5f9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac5f9-135">INPUTS</span></span>

### <span data-ttu-id="ac5f9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ac5f9-136">System.String</span></span>

### <span data-ttu-id="ac5f9-137">Microsoft. Azure. Commands. аттестация. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="ac5f9-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="ac5f9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac5f9-138">OUTPUTS</span></span>

### <span data-ttu-id="ac5f9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac5f9-139">System.Boolean</span></span>

## <span data-ttu-id="ac5f9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac5f9-140">NOTES</span></span>

## <span data-ttu-id="ac5f9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac5f9-141">RELATED LINKS</span></span>
