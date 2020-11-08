---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248386"
---
# <span data-ttu-id="e7804-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e7804-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="e7804-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7804-102">SYNOPSIS</span></span>
<span data-ttu-id="e7804-103">Удаление тома NetApp Files (ANF) для Azure.</span><span class="sxs-lookup"><span data-stu-id="e7804-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="e7804-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7804-104">SYNTAX</span></span>

### <span data-ttu-id="e7804-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7804-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7804-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7804-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7804-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7804-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7804-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7804-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7804-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7804-109">DESCRIPTION</span></span>
<span data-ttu-id="e7804-110">Командлет **Remove-AzNetAppFilesVolume** УДАЛЯЕТ том ANF.</span><span class="sxs-lookup"><span data-stu-id="e7804-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="e7804-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7804-111">EXAMPLES</span></span>

### <span data-ttu-id="e7804-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7804-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="e7804-113">Эта команда удаляет ANF Volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="e7804-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="e7804-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7804-114">PARAMETERS</span></span>

### <span data-ttu-id="e7804-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e7804-115">-AccountName</span></span>
<span data-ttu-id="e7804-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="e7804-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7804-117">-DefaultProfile</span></span>
<span data-ttu-id="e7804-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7804-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7804-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7804-119">-InputObject</span></span>
<span data-ttu-id="e7804-120">Объект тома, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e7804-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7804-121">-Name</span></span>
<span data-ttu-id="e7804-122">Имя ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="e7804-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7804-123">-PassThru</span></span>
<span data-ttu-id="e7804-124">Возвращает значение, указывающее, был ли успешно удален указанный том</span><span class="sxs-lookup"><span data-stu-id="e7804-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="e7804-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e7804-125">-PoolName</span></span>
<span data-ttu-id="e7804-126">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="e7804-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="e7804-127">-PoolObject</span></span>
<span data-ttu-id="e7804-128">Объект пула, содержащий том, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e7804-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7804-129">-ResourceGroupName</span></span>
<span data-ttu-id="e7804-130">Группа ресурсов ANFого тома</span><span class="sxs-lookup"><span data-stu-id="e7804-130">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7804-131">-ResourceId</span></span>
<span data-ttu-id="e7804-132">Идентификатор ресурса ANFого тома.</span><span class="sxs-lookup"><span data-stu-id="e7804-132">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7804-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7804-133">-Confirm</span></span>
<span data-ttu-id="e7804-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7804-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7804-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7804-135">-WhatIf</span></span>
<span data-ttu-id="e7804-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7804-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7804-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7804-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7804-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7804-138">CommonParameters</span></span>
<span data-ttu-id="e7804-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7804-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7804-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7804-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7804-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7804-141">INPUTS</span></span>

### <span data-ttu-id="e7804-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e7804-142">System.String</span></span>

### <span data-ttu-id="e7804-143">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e7804-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="e7804-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e7804-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e7804-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7804-145">OUTPUTS</span></span>

### <span data-ttu-id="e7804-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7804-146">System.Boolean</span></span>

## <span data-ttu-id="e7804-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7804-147">NOTES</span></span>

## <span data-ttu-id="e7804-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7804-148">RELATED LINKS</span></span>
