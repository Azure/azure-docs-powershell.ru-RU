---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 8665119abafe928f140f79b2cec8ee2e8fcfeff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561388"
---
# <span data-ttu-id="e197a-101">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e197a-101">Remove-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="e197a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e197a-102">SYNOPSIS</span></span>
<span data-ttu-id="e197a-103">Удаляет группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e197a-103">Removes an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e197a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e197a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e197a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e197a-105">DESCRIPTION</span></span>
<span data-ttu-id="e197a-106">Командлет **Remove-AzureRmSqlSyncGroup** удаляет группу синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e197a-106">The **Remove-AzureRmSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e197a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e197a-107">EXAMPLES</span></span>

### <span data-ttu-id="e197a-108">Пример 1: Удаление группы синхронизации</span><span class="sxs-lookup"><span data-stu-id="e197a-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="e197a-109">Эта команда удаляет группу синхронизации базы данных SQL Azure с именем syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="e197a-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="e197a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e197a-110">PARAMETERS</span></span>

### <span data-ttu-id="e197a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e197a-111">-DatabaseName</span></span>
<span data-ttu-id="e197a-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e197a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e197a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e197a-113">-DefaultProfile</span></span>
<span data-ttu-id="e197a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e197a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e197a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e197a-115">-Force</span></span>
<span data-ttu-id="e197a-116">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="e197a-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e197a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e197a-117">-Name</span></span>
<span data-ttu-id="e197a-118">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e197a-118">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e197a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e197a-119">-PassThru</span></span>
<span data-ttu-id="e197a-120">Определяет, возвращают ли удаленную группу синхронизации</span><span class="sxs-lookup"><span data-stu-id="e197a-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="e197a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e197a-121">-ResourceGroupName</span></span>
<span data-ttu-id="e197a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e197a-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e197a-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e197a-123">-ServerName</span></span>
<span data-ttu-id="e197a-124">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e197a-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e197a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e197a-125">-Confirm</span></span>
<span data-ttu-id="e197a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e197a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e197a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e197a-127">-WhatIf</span></span>
<span data-ttu-id="e197a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e197a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e197a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e197a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e197a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e197a-130">CommonParameters</span></span>
<span data-ttu-id="e197a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e197a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e197a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e197a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e197a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e197a-133">INPUTS</span></span>

### <span data-ttu-id="e197a-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="e197a-134">None</span></span>
<span data-ttu-id="e197a-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e197a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e197a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e197a-136">OUTPUTS</span></span>

### <span data-ttu-id="e197a-137">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e197a-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e197a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e197a-138">NOTES</span></span>

## <span data-ttu-id="e197a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e197a-139">RELATED LINKS</span></span>

[<span data-ttu-id="e197a-140">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e197a-140">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e197a-141">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e197a-141">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e197a-142">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e197a-142">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

