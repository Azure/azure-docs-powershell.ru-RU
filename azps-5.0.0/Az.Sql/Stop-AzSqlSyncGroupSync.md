---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248283"
---
# <span data-ttu-id="8e3e5-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="8e3e5-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="8e3e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3e5-103">Останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="8e3e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e3e5-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e3e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e3e5-105">DESCRIPTION</span></span>
<span data-ttu-id="8e3e5-106">Командлет **Stop-AzSqlSyncGroupSync** останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="8e3e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e3e5-107">EXAMPLES</span></span>

### <span data-ttu-id="8e3e5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e3e5-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="8e3e5-109">Эта команда останавливает синхронизацию, которая выполняется для группы синхронизации mysg.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="8e3e5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e3e5-110">PARAMETERS</span></span>

### <span data-ttu-id="8e3e5-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e3e5-111">-DatabaseName</span></span>
<span data-ttu-id="8e3e5-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3e5-113">-DefaultProfile</span></span>
<span data-ttu-id="8e3e5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8e3e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3e5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e3e5-115">-PassThru</span></span>
<span data-ttu-id="8e3e5-116">Определяет, возвращают ли группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="8e3e5-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="8e3e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e3e5-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e5-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8e3e5-119">-ServerName</span></span>
<span data-ttu-id="8e3e5-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-120">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e5-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3e5-121">-SyncGroupName</span></span>
<span data-ttu-id="8e3e5-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3e5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e3e5-123">-Confirm</span></span>
<span data-ttu-id="8e3e5-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e3e5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e3e5-125">-WhatIf</span></span>
<span data-ttu-id="8e3e5-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e3e5-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e3e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3e5-128">CommonParameters</span></span>
<span data-ttu-id="8e3e5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e3e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3e5-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e3e5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3e5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e3e5-131">INPUTS</span></span>

### <span data-ttu-id="8e3e5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8e3e5-132">System.String</span></span>

## <span data-ttu-id="8e3e5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e3e5-133">OUTPUTS</span></span>

### <span data-ttu-id="8e3e5-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="8e3e5-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="8e3e5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e3e5-135">NOTES</span></span>

## <span data-ttu-id="8e3e5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e3e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e3e5-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="8e3e5-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

