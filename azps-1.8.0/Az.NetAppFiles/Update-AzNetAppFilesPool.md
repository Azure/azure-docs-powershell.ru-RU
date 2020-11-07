---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesPool.md
ms.openlocfilehash: 3dd02a2dc0cf7090ba2711b6155d25038397ab9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730759"
---
# <span data-ttu-id="f4423-101">Update-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f4423-101">Update-AzNetAppFilesPool</span></span>

## <span data-ttu-id="f4423-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4423-102">SYNOPSIS</span></span>
<span data-ttu-id="f4423-103">Обновление пула файлов Azure NetApp (ANF) с помощью нового множества данных.</span><span class="sxs-lookup"><span data-stu-id="f4423-103">Updates an Azure NetApp Files (ANF) pool with the new data set.</span></span>

## <span data-ttu-id="f4423-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4423-104">SYNTAX</span></span>

### <span data-ttu-id="f4423-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4423-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4423-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4423-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String>
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4423-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4423-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -PoolSize <Int64> -ServiceLevel <String> -InputObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4423-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4423-108">DESCRIPTION</span></span>
<span data-ttu-id="f4423-109">Командлет **Update-AzNetAppFilesPool** изменяет пул ANF.</span><span class="sxs-lookup"><span data-stu-id="f4423-109">The **Update-AzNetAppFilesPool** cmdlet modifies an ANF pool.</span></span>

## <span data-ttu-id="f4423-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4423-110">EXAMPLES</span></span>

### <span data-ttu-id="f4423-111">Пример 1: изменение пула ANF</span><span class="sxs-lookup"><span data-stu-id="f4423-111">Example 1: Modify an ANF pool</span></span>
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

<span data-ttu-id="f4423-112">Эта команда изменяет для пула ANF "MyAnfPool" заданный размер и ServiceLevel.</span><span class="sxs-lookup"><span data-stu-id="f4423-112">This command changes the ANF pool "MyAnfPool" to have the given size and ServiceLevel.</span></span>

## <span data-ttu-id="f4423-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4423-113">PARAMETERS</span></span>

### <span data-ttu-id="f4423-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f4423-114">-AccountName</span></span>
<span data-ttu-id="f4423-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="f4423-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="f4423-116">-AccountObject</span></span>
<span data-ttu-id="f4423-117">Объект Account, содержащий пул для обновления.</span><span class="sxs-lookup"><span data-stu-id="f4423-117">The account object containing the pool to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4423-118">-DefaultProfile</span></span>
<span data-ttu-id="f4423-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4423-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4423-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4423-120">-InputObject</span></span>
<span data-ttu-id="f4423-121">Объект пула, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="f4423-121">The pool object to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-122">-Location</span><span class="sxs-lookup"><span data-stu-id="f4423-122">-Location</span></span>
<span data-ttu-id="f4423-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="f4423-123">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4423-124">-Name</span></span>
<span data-ttu-id="f4423-125">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="f4423-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-126">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="f4423-126">-PoolSize</span></span>
<span data-ttu-id="f4423-127">Размер пула ANF</span><span class="sxs-lookup"><span data-stu-id="f4423-127">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4423-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4423-129">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="f4423-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f4423-130">-ServiceLevel</span></span>
<span data-ttu-id="f4423-131">Уровень обслуживания пула ANF</span><span class="sxs-lookup"><span data-stu-id="f4423-131">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4423-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4423-132">-Confirm</span></span>
<span data-ttu-id="f4423-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4423-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4423-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4423-134">-WhatIf</span></span>
<span data-ttu-id="f4423-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4423-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4423-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4423-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4423-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4423-137">CommonParameters</span></span>
<span data-ttu-id="f4423-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4423-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f4423-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4423-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4423-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4423-140">INPUTS</span></span>

### <span data-ttu-id="f4423-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f4423-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f4423-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f4423-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f4423-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4423-143">OUTPUTS</span></span>

### <span data-ttu-id="f4423-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f4423-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f4423-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4423-145">NOTES</span></span>

## <span data-ttu-id="f4423-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4423-146">RELATED LINKS</span></span>
