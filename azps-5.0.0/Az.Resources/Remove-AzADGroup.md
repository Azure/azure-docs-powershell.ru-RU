---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 895974f12c7472cb93679cb27ca895ca40757f53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245889"
---
# <span data-ttu-id="32c1f-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="32c1f-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="32c1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="32c1f-103">Удаление группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32c1f-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="32c1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32c1f-104">SYNTAX</span></span>

### <span data-ttu-id="32c1f-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32c1f-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32c1f-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="32c1f-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32c1f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32c1f-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32c1f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="32c1f-109">Удаление группы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32c1f-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="32c1f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="32c1f-111">Пример 1: удаление группировки по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="32c1f-111">Example 1: Remove a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="32c1f-112">Удаляет из клиента группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="32c1f-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="32c1f-113">Пример 2: удаление группировки по конвейеру</span><span class="sxs-lookup"><span data-stu-id="32c1f-113">Example 2: Remove a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="32c1f-114">Получает группу с идентификатором объекта "85F89C90-780E-4AA6-9F4F-6F268D322EEE" и каналами, которые нужно Remove-AzADGroup, чтобы удалить группу из клиента.</span><span class="sxs-lookup"><span data-stu-id="32c1f-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="32c1f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32c1f-115">PARAMETERS</span></span>

### <span data-ttu-id="32c1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c1f-116">-DefaultProfile</span></span>
<span data-ttu-id="32c1f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32c1f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32c1f-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32c1f-118">-DisplayName</span></span>
<span data-ttu-id="32c1f-119">Отображаемое имя группы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="32c1f-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32c1f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="32c1f-120">-Force</span></span>
<span data-ttu-id="32c1f-121">Если этот элемент указан, подтверждение удаления группы не запрашивается.</span><span class="sxs-lookup"><span data-stu-id="32c1f-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

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

### <span data-ttu-id="32c1f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32c1f-122">-InputObject</span></span>
<span data-ttu-id="32c1f-123">Объектное представление удаляемой группы.</span><span class="sxs-lookup"><span data-stu-id="32c1f-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32c1f-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="32c1f-124">-ObjectId</span></span>
<span data-ttu-id="32c1f-125">Идентификатор объекта группы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="32c1f-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32c1f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32c1f-126">-PassThru</span></span>
<span data-ttu-id="32c1f-127">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="32c1f-127">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="32c1f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32c1f-128">-Confirm</span></span>
<span data-ttu-id="32c1f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32c1f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c1f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c1f-130">-WhatIf</span></span>
<span data-ttu-id="32c1f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32c1f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32c1f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32c1f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c1f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c1f-133">CommonParameters</span></span>
<span data-ttu-id="32c1f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32c1f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c1f-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32c1f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c1f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32c1f-136">INPUTS</span></span>

### <span data-ttu-id="32c1f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="32c1f-137">System.String</span></span>

### <span data-ttu-id="32c1f-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="32c1f-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="32c1f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32c1f-139">OUTPUTS</span></span>

### <span data-ttu-id="32c1f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32c1f-140">System.Boolean</span></span>

## <span data-ttu-id="32c1f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="32c1f-141">NOTES</span></span>

## <span data-ttu-id="32c1f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32c1f-142">RELATED LINKS</span></span>