---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: 040b08e328cb06629e706350fa14752fa6918954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563247"
---
# <span data-ttu-id="eb70d-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="eb70d-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="eb70d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb70d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb70d-103">Запуск синхронизации группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eb70d-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb70d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb70d-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb70d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb70d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb70d-106">Командлет **Start-AzureRmSqlSyncGroupSync** запускает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eb70d-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="eb70d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb70d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb70d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb70d-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="eb70d-109">Эта команда запускает круговую синхронизацию для группы синхронизации mysg.</span><span class="sxs-lookup"><span data-stu-id="eb70d-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="eb70d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb70d-110">PARAMETERS</span></span>

### <span data-ttu-id="eb70d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb70d-111">-DatabaseName</span></span>
<span data-ttu-id="eb70d-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eb70d-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb70d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb70d-113">-DefaultProfile</span></span>
<span data-ttu-id="eb70d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb70d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb70d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb70d-115">-PassThru</span></span>
<span data-ttu-id="eb70d-116">Определяет, возвращают ли группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="eb70d-116">Defines Whether return the sync group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb70d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb70d-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb70d-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb70d-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb70d-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="eb70d-119">-ServerName</span></span>
<span data-ttu-id="eb70d-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb70d-120">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb70d-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="eb70d-121">-SyncGroupName</span></span>
<span data-ttu-id="eb70d-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eb70d-122">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb70d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb70d-123">-Confirm</span></span>
<span data-ttu-id="eb70d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb70d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb70d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb70d-125">-WhatIf</span></span>
<span data-ttu-id="eb70d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb70d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb70d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb70d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb70d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb70d-128">CommonParameters</span></span>
<span data-ttu-id="eb70d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb70d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb70d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb70d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb70d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb70d-131">INPUTS</span></span>

### <span data-ttu-id="eb70d-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb70d-132">None</span></span>
<span data-ttu-id="eb70d-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb70d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb70d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb70d-134">OUTPUTS</span></span>

### <span data-ttu-id="eb70d-135">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="eb70d-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="eb70d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb70d-136">NOTES</span></span>

## <span data-ttu-id="eb70d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb70d-137">RELATED LINKS</span></span>

[<span data-ttu-id="eb70d-138">Остановить-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="eb70d-138">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

