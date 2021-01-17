---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 8f26023224e0f6d4a035f4671db7b45be57a3177
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422463"
---
# <span data-ttu-id="8d217-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8d217-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="8d217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d217-102">SYNOPSIS</span></span>
<span data-ttu-id="8d217-103">Обновляет пул файлов Azure NetApp (ANF) в соответствии с предоставленными необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="8d217-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="8d217-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d217-104">SYNTAX</span></span>

### <span data-ttu-id="8d217-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d217-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d217-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d217-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d217-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d217-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d217-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d217-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-QosType <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d217-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d217-109">DESCRIPTION</span></span>
<span data-ttu-id="8d217-110">Для пула ANF будет модификатор **Update-AzNetAppFilesPool.**</span><span class="sxs-lookup"><span data-stu-id="8d217-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="8d217-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d217-111">EXAMPLES</span></span>

### <span data-ttu-id="8d217-112">Пример 1. Изменение пула ANF</span><span class="sxs-lookup"><span data-stu-id="8d217-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="8d217-113">Эта команда изменяет пул ANF "MyAnfPool" на заданный размер и QosType.</span><span class="sxs-lookup"><span data-stu-id="8d217-113">This command changes the ANF pool "MyAnfPool" to have the given size and QosType.</span></span>

## <span data-ttu-id="8d217-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d217-114">PARAMETERS</span></span>

### <span data-ttu-id="8d217-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d217-115">-AccountName</span></span>
<span data-ttu-id="8d217-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8d217-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8d217-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8d217-117">-AccountObject</span></span>
<span data-ttu-id="8d217-118">Объект учетной записи, содержащий пул для обновления</span><span class="sxs-lookup"><span data-stu-id="8d217-118">The account object containing the pool to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d217-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d217-119">-DefaultProfile</span></span>
<span data-ttu-id="8d217-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d217-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d217-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d217-121">-InputObject</span></span>
<span data-ttu-id="8d217-122">Объект пула, который нужно обновить</span><span class="sxs-lookup"><span data-stu-id="8d217-122">The pool object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d217-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8d217-123">-Location</span></span>
<span data-ttu-id="8d217-124">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="8d217-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d217-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8d217-125">-Name</span></span>
<span data-ttu-id="8d217-126">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="8d217-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d217-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="8d217-127">-PoolSize</span></span>
<span data-ttu-id="8d217-128">Размер пула ANF</span><span class="sxs-lookup"><span data-stu-id="8d217-128">The size of the ANF pool</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d217-129">-QosType</span><span class="sxs-lookup"><span data-stu-id="8d217-129">-QosType</span></span>
<span data-ttu-id="8d217-130">Тип qos пула.</span><span class="sxs-lookup"><span data-stu-id="8d217-130">The qos type of the pool.</span></span> <span data-ttu-id="8d217-131">Возможные значения: "Авто", "Вручную"</span><span class="sxs-lookup"><span data-stu-id="8d217-131">Possible values include: 'Auto', 'Manual'</span></span>

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

### <span data-ttu-id="8d217-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d217-132">-ResourceGroupName</span></span>
<span data-ttu-id="8d217-133">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8d217-133">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8d217-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d217-134">-ResourceId</span></span>
<span data-ttu-id="8d217-135">ИД ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="8d217-135">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="8d217-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="8d217-136">-Tag</span></span>
<span data-ttu-id="8d217-137">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="8d217-137">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d217-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d217-138">-Confirm</span></span>
<span data-ttu-id="8d217-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8d217-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d217-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d217-140">-WhatIf</span></span>
<span data-ttu-id="8d217-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d217-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d217-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d217-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d217-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d217-143">CommonParameters</span></span>
<span data-ttu-id="8d217-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d217-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d217-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d217-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d217-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d217-146">INPUTS</span></span>

### <span data-ttu-id="8d217-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8d217-147">System.String</span></span>

### <span data-ttu-id="8d217-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8d217-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8d217-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8d217-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8d217-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d217-150">OUTPUTS</span></span>

### <span data-ttu-id="8d217-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8d217-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8d217-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d217-152">NOTES</span></span>

## <span data-ttu-id="8d217-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d217-153">RELATED LINKS</span></span>
