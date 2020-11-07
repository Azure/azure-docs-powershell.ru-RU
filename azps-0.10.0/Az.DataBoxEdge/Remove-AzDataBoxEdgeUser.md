---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 1d6c99a44e2163f2d441dcacc87cf202f334f330
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910433"
---
# <span data-ttu-id="54fee-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="54fee-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="54fee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54fee-102">SYNOPSIS</span></span>
<span data-ttu-id="54fee-103">Удаление пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="54fee-103">Removes a user on a device.</span></span>

## <span data-ttu-id="54fee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54fee-104">SYNTAX</span></span>

### <span data-ttu-id="54fee-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54fee-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fee-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fee-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fee-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fee-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fee-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54fee-108">DESCRIPTION</span></span>
<span data-ttu-id="54fee-109">Командлет **Remove-AzDataBoxEdgeUser** удаляет пользователя на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="54fee-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="54fee-110">Поддерживается создание только пользователей типа `Share` .</span><span class="sxs-lookup"><span data-stu-id="54fee-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="54fee-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54fee-111">EXAMPLES</span></span>

### <span data-ttu-id="54fee-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54fee-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="54fee-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54fee-113">PARAMETERS</span></span>

### <span data-ttu-id="54fee-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54fee-114">-AsJob</span></span>
<span data-ttu-id="54fee-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="54fee-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54fee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fee-116">-DefaultProfile</span></span>
<span data-ttu-id="54fee-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54fee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54fee-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="54fee-118">-DeviceName</span></span>
<span data-ttu-id="54fee-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="54fee-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54fee-120">-InputObject</span></span>
<span data-ttu-id="54fee-121">Объект input</span><span class="sxs-lookup"><span data-stu-id="54fee-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fee-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54fee-122">-Name</span></span>
<span data-ttu-id="54fee-123">Действительно</span><span class="sxs-lookup"><span data-stu-id="54fee-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fee-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54fee-124">-PassThru</span></span>
<span data-ttu-id="54fee-125">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="54fee-125">returns true if successful</span></span>

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

### <span data-ttu-id="54fee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fee-126">-ResourceGroupName</span></span>
<span data-ttu-id="54fee-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="54fee-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fee-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54fee-128">-ResourceId</span></span>
<span data-ttu-id="54fee-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="54fee-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fee-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54fee-130">-Confirm</span></span>
<span data-ttu-id="54fee-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54fee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fee-132">-WhatIf</span></span>
<span data-ttu-id="54fee-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54fee-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54fee-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54fee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fee-135">CommonParameters</span></span>
<span data-ttu-id="54fee-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54fee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fee-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54fee-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fee-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54fee-138">INPUTS</span></span>

### <span data-ttu-id="54fee-139">System. String</span><span class="sxs-lookup"><span data-stu-id="54fee-139">System.String</span></span>

### <span data-ttu-id="54fee-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="54fee-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="54fee-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54fee-141">OUTPUTS</span></span>

### <span data-ttu-id="54fee-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="54fee-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="54fee-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="54fee-143">NOTES</span></span>

## <span data-ttu-id="54fee-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54fee-144">RELATED LINKS</span></span>
