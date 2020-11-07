---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727882"
---
# <span data-ttu-id="c0584-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="c0584-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="c0584-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0584-102">SYNOPSIS</span></span>
<span data-ttu-id="c0584-103">Удаление аттестации.</span><span class="sxs-lookup"><span data-stu-id="c0584-103">Deletes an attestation.</span></span>

## <span data-ttu-id="c0584-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0584-104">SYNTAX</span></span>

### <span data-ttu-id="c0584-105">ByAvailableAttestation (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0584-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0584-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="c0584-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0584-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="c0584-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0584-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0584-108">DESCRIPTION</span></span>
<span data-ttu-id="c0584-109">Командлет Remove-AzAttestation удаляет указанную аттестацию.</span><span class="sxs-lookup"><span data-stu-id="c0584-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="c0584-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0584-110">EXAMPLES</span></span>

### <span data-ttu-id="c0584-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0584-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="c0584-112">Удаление аттестации "пример" из текущей подписки и группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="c0584-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="c0584-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0584-113">PARAMETERS</span></span>

### <span data-ttu-id="c0584-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0584-114">-AsJob</span></span>
<span data-ttu-id="c0584-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c0584-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0584-116">-DefaultProfile</span></span>
<span data-ttu-id="c0584-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0584-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0584-118">-InputObject</span></span>
<span data-ttu-id="c0584-119">Объект аттестации, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c0584-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0584-120">-Name</span></span>
<span data-ttu-id="c0584-121">Указывает имя подтверждения для удаления.</span><span class="sxs-lookup"><span data-stu-id="c0584-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0584-122">-PassThru</span></span>
<span data-ttu-id="c0584-123">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0584-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c0584-124">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="c0584-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0584-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0584-126">Указывает имя группы ресурсов для аттестации Azure, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c0584-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0584-127">-ResourceId</span></span>
<span data-ttu-id="c0584-128">Идентификатор ресурса аттестации.</span><span class="sxs-lookup"><span data-stu-id="c0584-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0584-129">-Confirm</span></span>
<span data-ttu-id="c0584-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0584-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0584-131">-WhatIf</span></span>
<span data-ttu-id="c0584-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0584-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0584-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0584-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0584-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0584-134">CommonParameters</span></span>
<span data-ttu-id="c0584-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0584-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0584-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0584-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0584-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0584-137">INPUTS</span></span>

### <span data-ttu-id="c0584-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c0584-138">System.String</span></span>

### <span data-ttu-id="c0584-139">Microsoft. Azure. Commands. аттестация. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="c0584-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="c0584-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0584-140">OUTPUTS</span></span>

### <span data-ttu-id="c0584-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0584-141">System.Boolean</span></span>

## <span data-ttu-id="c0584-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0584-142">NOTES</span></span>

## <span data-ttu-id="c0584-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0584-143">RELATED LINKS</span></span>
