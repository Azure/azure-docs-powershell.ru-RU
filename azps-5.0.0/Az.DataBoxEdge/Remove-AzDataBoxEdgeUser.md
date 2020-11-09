---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314183"
---
# <span data-ttu-id="b70a4-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b70a4-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="b70a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b70a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b70a4-103">Удаление пользователя на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b70a4-103">Removes a user on a device.</span></span>

## <span data-ttu-id="b70a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b70a4-104">SYNTAX</span></span>

### <span data-ttu-id="b70a4-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b70a4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b70a4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b70a4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b70a4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b70a4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b70a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b70a4-108">DESCRIPTION</span></span>
<span data-ttu-id="b70a4-109">Командлет **Remove-AzDataBoxEdgeUser** удаляет пользователя на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="b70a4-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="b70a4-110">Поддерживается создание только пользователей типа `Share` .</span><span class="sxs-lookup"><span data-stu-id="b70a4-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="b70a4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b70a4-111">EXAMPLES</span></span>

### <span data-ttu-id="b70a4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b70a4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="b70a4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b70a4-113">PARAMETERS</span></span>

### <span data-ttu-id="b70a4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b70a4-114">-AsJob</span></span>
<span data-ttu-id="b70a4-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b70a4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b70a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70a4-116">-DefaultProfile</span></span>
<span data-ttu-id="b70a4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b70a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b70a4-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="b70a4-118">-DeviceName</span></span>
<span data-ttu-id="b70a4-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b70a4-119">Device Name</span></span>

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

### <span data-ttu-id="b70a4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b70a4-120">-InputObject</span></span>
<span data-ttu-id="b70a4-121">Объект input</span><span class="sxs-lookup"><span data-stu-id="b70a4-121">Input Object</span></span>

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

### <span data-ttu-id="b70a4-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b70a4-122">-Name</span></span>
<span data-ttu-id="b70a4-123">Действительно</span><span class="sxs-lookup"><span data-stu-id="b70a4-123">Username</span></span>

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

### <span data-ttu-id="b70a4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b70a4-124">-PassThru</span></span>
<span data-ttu-id="b70a4-125">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="b70a4-125">returns true if successful</span></span>

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

### <span data-ttu-id="b70a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="b70a4-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b70a4-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b70a4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b70a4-128">-ResourceId</span></span>
<span data-ttu-id="b70a4-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b70a4-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="b70a4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b70a4-130">-Confirm</span></span>
<span data-ttu-id="b70a4-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b70a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b70a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b70a4-132">-WhatIf</span></span>
<span data-ttu-id="b70a4-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b70a4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b70a4-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b70a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b70a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70a4-135">CommonParameters</span></span>
<span data-ttu-id="b70a4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b70a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70a4-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b70a4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70a4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b70a4-138">INPUTS</span></span>

### <span data-ttu-id="b70a4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b70a4-139">System.String</span></span>

### <span data-ttu-id="b70a4-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="b70a4-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="b70a4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b70a4-141">OUTPUTS</span></span>

### <span data-ttu-id="b70a4-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="b70a4-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="b70a4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="b70a4-143">NOTES</span></span>

## <span data-ttu-id="b70a4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b70a4-144">RELATED LINKS</span></span>
