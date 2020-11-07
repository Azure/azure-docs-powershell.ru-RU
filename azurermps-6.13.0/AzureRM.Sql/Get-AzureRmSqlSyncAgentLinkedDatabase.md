---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 11c444e92c6377e0a0df5aaa324ee162647784a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734107"
---
# <span data-ttu-id="91e69-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="91e69-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="91e69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91e69-102">SYNOPSIS</span></span>
<span data-ttu-id="91e69-103">Возвращает сведения о базах данных SQL Server, связанных агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91e69-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91e69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91e69-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91e69-105">DESCRIPTION</span></span>
<span data-ttu-id="91e69-106">Командлет **Get-AzureRmSqlSyncAgentLinkedDatabases** возвращает сведения о базах данных SQL Server, связанных агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91e69-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="91e69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91e69-107">EXAMPLES</span></span>

### <span data-ttu-id="91e69-108">Пример 1: получение связанных баз данных SQL Server для агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91e69-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="91e69-109">Эта команда возвращает связанные базы данных SQL Server, связанные с агентом синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="91e69-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="91e69-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91e69-110">PARAMETERS</span></span>

### <span data-ttu-id="91e69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e69-111">-DefaultProfile</span></span>
<span data-ttu-id="91e69-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="91e69-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91e69-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e69-113">-ResourceGroupName</span></span>
<span data-ttu-id="91e69-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91e69-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="91e69-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="91e69-115">-ServerName</span></span>
<span data-ttu-id="91e69-116">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91e69-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="91e69-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="91e69-117">-SyncAgentName</span></span>
<span data-ttu-id="91e69-118">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91e69-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91e69-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e69-119">CommonParameters</span></span>
<span data-ttu-id="91e69-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91e69-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e69-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e69-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e69-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91e69-122">INPUTS</span></span>

### <span data-ttu-id="91e69-123">System. String</span><span class="sxs-lookup"><span data-stu-id="91e69-123">System.String</span></span>

## <span data-ttu-id="91e69-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91e69-124">OUTPUTS</span></span>

### <span data-ttu-id="91e69-125">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="91e69-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="91e69-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="91e69-126">NOTES</span></span>

## <span data-ttu-id="91e69-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91e69-127">RELATED LINKS</span></span>
