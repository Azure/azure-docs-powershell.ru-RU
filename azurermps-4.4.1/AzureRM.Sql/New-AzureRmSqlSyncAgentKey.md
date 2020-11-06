---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: 254f2def5a1be57840ea195f326534ce883870df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565110"
---
# <span data-ttu-id="2c260-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2c260-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="2c260-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c260-102">SYNOPSIS</span></span>
<span data-ttu-id="2c260-103">Создание ключа агента синхронизации SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c260-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c260-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c260-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c260-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c260-105">DESCRIPTION</span></span>
<span data-ttu-id="2c260-106">Командлет **New-AzureRmSqlSyncAgentKey** создает ключ агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2c260-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2c260-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c260-107">EXAMPLES</span></span>

### <span data-ttu-id="2c260-108">Пример 1: создание ключа агента синхронизации для агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2c260-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2c260-109">Эта команда создает ключ агента синхронизации для агента Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="2c260-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2c260-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c260-110">PARAMETERS</span></span>

### <span data-ttu-id="2c260-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c260-111">-Confirm</span></span>
<span data-ttu-id="2c260-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c260-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c260-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c260-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c260-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c260-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c260-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2c260-115">-ServerName</span></span>
<span data-ttu-id="2c260-116">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2c260-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2c260-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2c260-117">-SyncAgentName</span></span>
<span data-ttu-id="2c260-118">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2c260-118">The sync agent name.</span></span>

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

### <span data-ttu-id="2c260-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c260-119">-WhatIf</span></span>
<span data-ttu-id="2c260-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c260-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c260-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c260-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c260-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c260-122">-DefaultProfile</span></span>
<span data-ttu-id="2c260-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c260-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c260-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c260-124">CommonParameters</span></span>
<span data-ttu-id="2c260-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c260-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c260-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c260-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c260-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c260-127">INPUTS</span></span>

## <span data-ttu-id="2c260-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c260-128">OUTPUTS</span></span>

### <span data-ttu-id="2c260-129">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2c260-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2c260-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c260-130">NOTES</span></span>

## <span data-ttu-id="2c260-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c260-131">RELATED LINKS</span></span>

