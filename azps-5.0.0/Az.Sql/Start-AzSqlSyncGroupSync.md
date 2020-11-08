---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246958"
---
# <span data-ttu-id="216b8-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="216b8-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="216b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="216b8-102">SYNOPSIS</span></span>
<span data-ttu-id="216b8-103">Запуск синхронизации группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="216b8-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="216b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="216b8-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="216b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="216b8-105">DESCRIPTION</span></span>
<span data-ttu-id="216b8-106">Командлет **Start-AzSqlSyncGroupSync** запускает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="216b8-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="216b8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="216b8-107">EXAMPLES</span></span>

### <span data-ttu-id="216b8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="216b8-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="216b8-109">Эта команда запускает круговую синхронизацию для группы синхронизации mysg.</span><span class="sxs-lookup"><span data-stu-id="216b8-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="216b8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="216b8-110">PARAMETERS</span></span>

### <span data-ttu-id="216b8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="216b8-111">-DatabaseName</span></span>
<span data-ttu-id="216b8-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="216b8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="216b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216b8-113">-DefaultProfile</span></span>
<span data-ttu-id="216b8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="216b8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="216b8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="216b8-115">-PassThru</span></span>
<span data-ttu-id="216b8-116">Определяет, возвращают ли группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="216b8-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="216b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="216b8-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="216b8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="216b8-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="216b8-119">-ServerName</span></span>
<span data-ttu-id="216b8-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="216b8-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="216b8-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="216b8-121">-SyncGroupName</span></span>
<span data-ttu-id="216b8-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="216b8-122">The sync group name.</span></span>

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

### <span data-ttu-id="216b8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="216b8-123">-Confirm</span></span>
<span data-ttu-id="216b8-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="216b8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216b8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216b8-125">-WhatIf</span></span>
<span data-ttu-id="216b8-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="216b8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216b8-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="216b8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216b8-128">CommonParameters</span></span>
<span data-ttu-id="216b8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="216b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216b8-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="216b8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216b8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="216b8-131">INPUTS</span></span>

### <span data-ttu-id="216b8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="216b8-132">System.String</span></span>

## <span data-ttu-id="216b8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="216b8-133">OUTPUTS</span></span>

### <span data-ttu-id="216b8-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="216b8-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="216b8-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="216b8-135">NOTES</span></span>

## <span data-ttu-id="216b8-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="216b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="216b8-137">Остановить-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="216b8-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

