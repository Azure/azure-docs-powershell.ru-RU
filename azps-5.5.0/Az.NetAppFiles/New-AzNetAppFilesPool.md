---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: e1ebab6e0b32c6358defee30512185868581b6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218905"
---
# <span data-ttu-id="75bf8-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="75bf8-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="75bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="75bf8-103">Создает новый пул файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="75bf8-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="75bf8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75bf8-104">SYNTAX</span></span>

### <span data-ttu-id="75bf8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75bf8-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75bf8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75bf8-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-QosType <String>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75bf8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75bf8-107">DESCRIPTION</span></span>
<span data-ttu-id="75bf8-108">Для создания пула ANF будет создаваться **cmdlet New-AzNetAppFilesPool.**</span><span class="sxs-lookup"><span data-stu-id="75bf8-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="75bf8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75bf8-109">EXAMPLES</span></span>

### <span data-ttu-id="75bf8-110">Пример 1. Создание пула ANF</span><span class="sxs-lookup"><span data-stu-id="75bf8-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium" -QosType "Auto"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="75bf8-111">Эта команда создает новый пул ANF "MyAnfPool" в учетной записи MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="75bf8-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="75bf8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75bf8-112">PARAMETERS</span></span>

### <span data-ttu-id="75bf8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75bf8-113">-AccountName</span></span>
<span data-ttu-id="75bf8-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="75bf8-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="75bf8-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="75bf8-115">-AccountObject</span></span>
<span data-ttu-id="75bf8-116">Учетная запись для нового объекта пула</span><span class="sxs-lookup"><span data-stu-id="75bf8-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="75bf8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75bf8-117">-DefaultProfile</span></span>
<span data-ttu-id="75bf8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75bf8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75bf8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="75bf8-119">-Location</span></span>
<span data-ttu-id="75bf8-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="75bf8-120">The location of the resource</span></span>

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

### <span data-ttu-id="75bf8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="75bf8-121">-Name</span></span>
<span data-ttu-id="75bf8-122">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="75bf8-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bf8-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="75bf8-123">-PoolSize</span></span>
<span data-ttu-id="75bf8-124">Размер пула ANF</span><span class="sxs-lookup"><span data-stu-id="75bf8-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bf8-125">-QosType</span><span class="sxs-lookup"><span data-stu-id="75bf8-125">-QosType</span></span>
<span data-ttu-id="75bf8-126">Тип qos пула.</span><span class="sxs-lookup"><span data-stu-id="75bf8-126">The qos type of the pool.</span></span> <span data-ttu-id="75bf8-127">Возможные значения: "Авто", "Вручную"</span><span class="sxs-lookup"><span data-stu-id="75bf8-127">Possible values include: 'Auto', 'Manual'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Auto
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bf8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75bf8-128">-ResourceGroupName</span></span>
<span data-ttu-id="75bf8-129">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="75bf8-129">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="75bf8-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="75bf8-130">-ServiceLevel</span></span>
<span data-ttu-id="75bf8-131">Уровень обслуживания пула ANF</span><span class="sxs-lookup"><span data-stu-id="75bf8-131">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75bf8-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="75bf8-132">-Tag</span></span>
<span data-ttu-id="75bf8-133">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="75bf8-133">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="75bf8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75bf8-134">-Confirm</span></span>
<span data-ttu-id="75bf8-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="75bf8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75bf8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bf8-136">-WhatIf</span></span>
<span data-ttu-id="75bf8-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75bf8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75bf8-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="75bf8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75bf8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bf8-139">CommonParameters</span></span>
<span data-ttu-id="75bf8-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75bf8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bf8-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75bf8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bf8-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75bf8-142">INPUTS</span></span>

### <span data-ttu-id="75bf8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="75bf8-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="75bf8-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75bf8-144">OUTPUTS</span></span>

### <span data-ttu-id="75bf8-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="75bf8-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="75bf8-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75bf8-146">NOTES</span></span>

## <span data-ttu-id="75bf8-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75bf8-147">RELATED LINKS</span></span>
