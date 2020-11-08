---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: f3b1a6180fb59b3c44942459e09a22a333fc9720
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079534"
---
# <span data-ttu-id="0a899-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0a899-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="0a899-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a899-102">SYNOPSIS</span></span>
<span data-ttu-id="0a899-103">Создание нового пула файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="0a899-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="0a899-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a899-104">SYNTAX</span></span>

### <span data-ttu-id="0a899-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a899-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a899-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a899-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a899-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a899-107">DESCRIPTION</span></span>
<span data-ttu-id="0a899-108">Командлет **New-AzNetAppFilesPool** создает пул ANF.</span><span class="sxs-lookup"><span data-stu-id="0a899-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="0a899-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a899-109">EXAMPLES</span></span>

### <span data-ttu-id="0a899-110">Пример 1: создание пула ANF</span><span class="sxs-lookup"><span data-stu-id="0a899-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="0a899-111">Эта команда создает новый пул ANF "MyAnfPool" в учетной записи "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="0a899-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="0a899-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a899-112">PARAMETERS</span></span>

### <span data-ttu-id="0a899-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="0a899-113">-AccountName</span></span>
<span data-ttu-id="0a899-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0a899-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="0a899-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0a899-115">-AccountObject</span></span>
<span data-ttu-id="0a899-116">Учетная запись для нового объекта пула</span><span class="sxs-lookup"><span data-stu-id="0a899-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="0a899-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a899-117">-DefaultProfile</span></span>
<span data-ttu-id="0a899-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a899-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a899-119">-Location</span><span class="sxs-lookup"><span data-stu-id="0a899-119">-Location</span></span>
<span data-ttu-id="0a899-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a899-120">The location of the resource</span></span>

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

### <span data-ttu-id="0a899-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a899-121">-Name</span></span>
<span data-ttu-id="0a899-122">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="0a899-122">The name of the ANF pool</span></span>

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

### <span data-ttu-id="0a899-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="0a899-123">-PoolSize</span></span>
<span data-ttu-id="0a899-124">Размер пула ANF</span><span class="sxs-lookup"><span data-stu-id="0a899-124">The size of the ANF pool</span></span>

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

### <span data-ttu-id="0a899-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a899-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a899-126">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0a899-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0a899-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="0a899-127">-ServiceLevel</span></span>
<span data-ttu-id="0a899-128">Уровень обслуживания пула ANF</span><span class="sxs-lookup"><span data-stu-id="0a899-128">The service level of the ANF pool</span></span>

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

### <span data-ttu-id="0a899-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="0a899-129">-Tag</span></span>
<span data-ttu-id="0a899-130">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="0a899-130">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="0a899-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a899-131">-Confirm</span></span>
<span data-ttu-id="0a899-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a899-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a899-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a899-133">-WhatIf</span></span>
<span data-ttu-id="0a899-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a899-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a899-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a899-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a899-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a899-136">CommonParameters</span></span>
<span data-ttu-id="0a899-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a899-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a899-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a899-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a899-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a899-139">INPUTS</span></span>

### <span data-ttu-id="0a899-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0a899-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0a899-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a899-141">OUTPUTS</span></span>

### <span data-ttu-id="0a899-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0a899-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="0a899-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a899-143">NOTES</span></span>

## <span data-ttu-id="0a899-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a899-144">RELATED LINKS</span></span>
