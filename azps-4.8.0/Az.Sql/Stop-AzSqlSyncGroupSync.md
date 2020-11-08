---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080226"
---
# <span data-ttu-id="bed66-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="bed66-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="bed66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bed66-102">SYNOPSIS</span></span>
<span data-ttu-id="bed66-103">Останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bed66-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="bed66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bed66-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bed66-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bed66-105">DESCRIPTION</span></span>
<span data-ttu-id="bed66-106">Командлет **Stop-AzSqlSyncGroupSync** останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bed66-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="bed66-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bed66-107">EXAMPLES</span></span>

### <span data-ttu-id="bed66-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bed66-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="bed66-109">Эта команда останавливает синхронизацию, которая выполняется для группы синхронизации mysg.</span><span class="sxs-lookup"><span data-stu-id="bed66-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="bed66-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bed66-110">PARAMETERS</span></span>

### <span data-ttu-id="bed66-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bed66-111">-DatabaseName</span></span>
<span data-ttu-id="bed66-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bed66-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="bed66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed66-113">-DefaultProfile</span></span>
<span data-ttu-id="bed66-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bed66-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bed66-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bed66-115">-PassThru</span></span>
<span data-ttu-id="bed66-116">Определяет, возвращают ли группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="bed66-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="bed66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed66-117">-ResourceGroupName</span></span>
<span data-ttu-id="bed66-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bed66-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="bed66-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bed66-119">-ServerName</span></span>
<span data-ttu-id="bed66-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bed66-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="bed66-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="bed66-121">-SyncGroupName</span></span>
<span data-ttu-id="bed66-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="bed66-122">The sync group name.</span></span>

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

### <span data-ttu-id="bed66-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bed66-123">-Confirm</span></span>
<span data-ttu-id="bed66-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bed66-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bed66-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bed66-125">-WhatIf</span></span>
<span data-ttu-id="bed66-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bed66-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bed66-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bed66-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bed66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed66-128">CommonParameters</span></span>
<span data-ttu-id="bed66-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bed66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed66-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bed66-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed66-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bed66-131">INPUTS</span></span>

### <span data-ttu-id="bed66-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bed66-132">System.String</span></span>

## <span data-ttu-id="bed66-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bed66-133">OUTPUTS</span></span>

### <span data-ttu-id="bed66-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="bed66-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="bed66-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bed66-135">NOTES</span></span>

## <span data-ttu-id="bed66-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bed66-136">RELATED LINKS</span></span>

[<span data-ttu-id="bed66-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="bed66-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

