---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 9cd213aea4e6211f52b076fca753385aefb1b449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562504"
---
# <span data-ttu-id="ebe3c-101">Stop-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ebe3c-101">Stop-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="ebe3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe3c-103">Останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-103">Stops a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebe3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebe3c-104">SYNTAX</span></span>

```
Stop-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebe3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe3c-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe3c-106">Командлет **Stop-AzureRmSqlSyncGroupSync** останавливает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-106">The **Stop-AzureRmSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="ebe3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebe3c-107">EXAMPLES</span></span>

### <span data-ttu-id="ebe3c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebe3c-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="ebe3c-109">Эта команда останавливает синхронизацию, которая выполняется для группы синхронизации mysg.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="ebe3c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebe3c-110">PARAMETERS</span></span>

### <span data-ttu-id="ebe3c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebe3c-111">-DatabaseName</span></span>
<span data-ttu-id="ebe3c-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ebe3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe3c-113">-DefaultProfile</span></span>
<span data-ttu-id="ebe3c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ebe3c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe3c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebe3c-115">-PassThru</span></span>
<span data-ttu-id="ebe3c-116">Определяет, возвращают ли группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="ebe3c-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="ebe3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="ebe3c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ebe3c-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ebe3c-119">-ServerName</span></span>
<span data-ttu-id="ebe3c-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ebe3c-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe3c-121">-SyncGroupName</span></span>
<span data-ttu-id="ebe3c-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-122">The sync group name.</span></span>

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

### <span data-ttu-id="ebe3c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebe3c-123">-Confirm</span></span>
<span data-ttu-id="ebe3c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe3c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebe3c-125">-WhatIf</span></span>
<span data-ttu-id="ebe3c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebe3c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe3c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe3c-128">CommonParameters</span></span>
<span data-ttu-id="ebe3c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe3c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe3c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe3c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebe3c-131">INPUTS</span></span>

### <span data-ttu-id="ebe3c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ebe3c-132">System.String</span></span>

## <span data-ttu-id="ebe3c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe3c-133">OUTPUTS</span></span>

### <span data-ttu-id="ebe3c-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="ebe3c-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="ebe3c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebe3c-135">NOTES</span></span>

## <span data-ttu-id="ebe3c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebe3c-136">RELATED LINKS</span></span>

[<span data-ttu-id="ebe3c-137">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="ebe3c-137">Start-AzureRmSqlSyncGroupSync</span></span>](./Start-AzureRmSqlSyncGroupSync.md)

