---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 34aec11e5f4bd2ee0aef37a4287544081bb9a87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566670"
---
# <span data-ttu-id="71ff0-101">Update-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="71ff0-101">Update-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="71ff0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="71ff0-103">Обновите схему синхронизации для базы данных участника синхронизации или базы данных концентратора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="71ff0-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="71ff0-104">Она будет получать последнюю схему базы данных из реальной базы данных, а затем использовать ее для обновления схемы, кэшированной с помощью базы данных метаданных синхронизации.</span><span class="sxs-lookup"><span data-stu-id="71ff0-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="71ff0-105">Если задано значение "SyncMemberName", будет обновлена схема базы данных участника; в противном случае будет обновлена схема базы данных основного сервера.</span><span class="sxs-lookup"><span data-stu-id="71ff0-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ff0-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71ff0-106">SYNTAX</span></span>

```
Update-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ff0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71ff0-107">DESCRIPTION</span></span>
<span data-ttu-id="71ff0-108">Командлет **Update-AzureRmSqlSyncSchema** обновляет схему синхронизации для базы данных участника синхронизации или базы данных концентратора синхронизации.</span><span class="sxs-lookup"><span data-stu-id="71ff0-108">The **Update-AzureRmSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="71ff0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71ff0-109">EXAMPLES</span></span>

### <span data-ttu-id="71ff0-110">Пример 1: обновление схемы синхронизации для базы данных-концентратора</span><span class="sxs-lookup"><span data-stu-id="71ff0-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="71ff0-111">Эта команда обновляет схему синхронизации для базы данных Hub в группе "Синхронизация" syncGroup01</span><span class="sxs-lookup"><span data-stu-id="71ff0-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="71ff0-112">Пример 2: обновление схемы синхронизации для базы данных участника</span><span class="sxs-lookup"><span data-stu-id="71ff0-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="71ff0-113">Эта команда обновляет схему синхронизации для базы данных пользователей в элементе Sync syncMember01</span><span class="sxs-lookup"><span data-stu-id="71ff0-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="71ff0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71ff0-114">PARAMETERS</span></span>

### <span data-ttu-id="71ff0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71ff0-115">-Confirm</span></span>
<span data-ttu-id="71ff0-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71ff0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ff0-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71ff0-117">-DatabaseName</span></span>
<span data-ttu-id="71ff0-118">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="71ff0-118">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="71ff0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71ff0-119">-PassThru</span></span>
<span data-ttu-id="71ff0-120">Определяет, будет ли возвращена группа синхронизации, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71ff0-120">Defines Whether return the sync group this cmdlet works on</span></span>

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

### <span data-ttu-id="71ff0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ff0-121">-ResourceGroupName</span></span>
<span data-ttu-id="71ff0-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71ff0-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="71ff0-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="71ff0-123">-ServerName</span></span>
<span data-ttu-id="71ff0-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="71ff0-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="71ff0-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="71ff0-125">-SyncGroupName</span></span>
<span data-ttu-id="71ff0-126">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="71ff0-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ff0-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="71ff0-127">-SyncMemberName</span></span>
<span data-ttu-id="71ff0-128">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="71ff0-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ff0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ff0-129">-WhatIf</span></span>
<span data-ttu-id="71ff0-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71ff0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71ff0-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71ff0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ff0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ff0-132">-DefaultProfile</span></span>
<span data-ttu-id="71ff0-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71ff0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ff0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ff0-134">CommonParameters</span></span>
<span data-ttu-id="71ff0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71ff0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ff0-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ff0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ff0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71ff0-137">INPUTS</span></span>

## <span data-ttu-id="71ff0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71ff0-138">OUTPUTS</span></span>

### <span data-ttu-id="71ff0-139">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="71ff0-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="71ff0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="71ff0-140">NOTES</span></span>

## <span data-ttu-id="71ff0-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71ff0-141">RELATED LINKS</span></span>

