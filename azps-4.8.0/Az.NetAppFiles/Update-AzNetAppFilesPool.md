---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: e63812f1972effd7956911861e5c6e07436fd4c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079535"
---
# <span data-ttu-id="279d6-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="279d6-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="279d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="279d6-102">SYNOPSIS</span></span>
<span data-ttu-id="279d6-103">Обновляет пул файлов Azure NetApp (ANF) в соответствии с необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="279d6-103">Updates an Azure NetApp Files (ANF) pool according to the optional modifiers provided.</span></span>

## <span data-ttu-id="279d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="279d6-104">SYNTAX</span></span>

### <span data-ttu-id="279d6-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="279d6-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> [-Location <String>] -AccountName <String> -Name <String>
 [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279d6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279d6-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="279d6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="279d6-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279d6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279d6-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="279d6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="279d6-109">DESCRIPTION</span></span>
<span data-ttu-id="279d6-110">Командлет **Update-AzNetAppFilesPool** изменяет пул ANF.</span><span class="sxs-lookup"><span data-stu-id="279d6-110">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="279d6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="279d6-111">EXAMPLES</span></span>

### <span data-ttu-id="279d6-112">Пример 1: изменение пула ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-112">Example 1: Modify an ANF pool</span></span>
```
PS C:\>Update-AzNetAppFilesPool -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolSize 4398046511104 -ServiceLevel "Standard"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
Size              : 4398046511104
ServiceLevel      : Standard
ProvisioningState : Succeeded
```

<span data-ttu-id="279d6-113">Эта команда изменяет для пула ANF "MyAnfPool" заданный размер и ServiceLevel.</span><span class="sxs-lookup"><span data-stu-id="279d6-113">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="279d6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="279d6-114">PARAMETERS</span></span>

### <span data-ttu-id="279d6-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="279d6-115">-AccountName</span></span>
<span data-ttu-id="279d6-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="279d6-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="279d6-117">-AccountObject</span></span>
<span data-ttu-id="279d6-118">Объект Account, содержащий пул для обновления.</span><span class="sxs-lookup"><span data-stu-id="279d6-118">The account object containing the pool to update</span></span>

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

### <span data-ttu-id="279d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279d6-119">-DefaultProfile</span></span>
<span data-ttu-id="279d6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="279d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279d6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279d6-121">-InputObject</span></span>
<span data-ttu-id="279d6-122">Объект пула, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="279d6-122">The pool object to update</span></span>

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

### <span data-ttu-id="279d6-123">-Location</span><span class="sxs-lookup"><span data-stu-id="279d6-123">-Location</span></span>
<span data-ttu-id="279d6-124">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="279d6-124">The location of the resource</span></span>

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

### <span data-ttu-id="279d6-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="279d6-125">-Name</span></span>
<span data-ttu-id="279d6-126">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="279d6-127">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="279d6-127">-PoolSize</span></span>
<span data-ttu-id="279d6-128">Размер пула ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-128">The size of the ANF pool</span></span>

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

### <span data-ttu-id="279d6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279d6-129">-ResourceGroupName</span></span>
<span data-ttu-id="279d6-130">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="279d6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279d6-131">-ResourceId</span></span>
<span data-ttu-id="279d6-132">Идентификатор ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-132">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="279d6-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="279d6-133">-ServiceLevel</span></span>
<span data-ttu-id="279d6-134">Уровень обслуживания пула ANF</span><span class="sxs-lookup"><span data-stu-id="279d6-134">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="279d6-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="279d6-135">-Tag</span></span>
<span data-ttu-id="279d6-136">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="279d6-136">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="279d6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="279d6-137">-Confirm</span></span>
<span data-ttu-id="279d6-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="279d6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279d6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279d6-139">-WhatIf</span></span>
<span data-ttu-id="279d6-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="279d6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279d6-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="279d6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279d6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279d6-142">CommonParameters</span></span>
<span data-ttu-id="279d6-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="279d6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279d6-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="279d6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279d6-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="279d6-145">INPUTS</span></span>

### <span data-ttu-id="279d6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="279d6-146">System.String</span></span>

### <span data-ttu-id="279d6-147">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="279d6-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="279d6-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="279d6-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="279d6-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="279d6-149">OUTPUTS</span></span>

### <span data-ttu-id="279d6-150">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="279d6-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="279d6-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="279d6-151">NOTES</span></span>

## <span data-ttu-id="279d6-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="279d6-152">RELATED LINKS</span></span>
