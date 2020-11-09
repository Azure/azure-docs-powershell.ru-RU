---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313160"
---
# <span data-ttu-id="7d465-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="7d465-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="7d465-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d465-102">SYNOPSIS</span></span>
<span data-ttu-id="7d465-103">Создает объект DatabaseInfo для службы миграции баз данных Azure, указывающий источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="7d465-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="7d465-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d465-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d465-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d465-105">DESCRIPTION</span></span>
<span data-ttu-id="7d465-106">Командлет New-AzDataMigrationDatabaseInfo создает объект DatabaseInfo, указывающий экземпляр исходной базы данных, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="7d465-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="7d465-107">Имя базы данных берется из входного параметра.</span><span class="sxs-lookup"><span data-stu-id="7d465-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="7d465-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d465-108">EXAMPLES</span></span>

### <span data-ttu-id="7d465-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d465-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="7d465-110">В предыдущем примере создается новый объект DatabaseInfo для **AdventureWorks2016** исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7d465-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="7d465-111">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7d465-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="7d465-112">Вы можете подтвердить свое состояние входа с помощью командлета Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="7d465-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="7d465-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d465-113">PARAMETERS</span></span>

### <span data-ttu-id="7d465-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d465-114">-DefaultProfile</span></span>
<span data-ttu-id="7d465-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d465-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d465-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d465-116">-SourceDatabaseName</span></span>
<span data-ttu-id="7d465-117">Имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7d465-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d465-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d465-118">CommonParameters</span></span>
<span data-ttu-id="7d465-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d465-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d465-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d465-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d465-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d465-121">INPUTS</span></span>

### <span data-ttu-id="7d465-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="7d465-122">None</span></span>

## <span data-ttu-id="7d465-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d465-123">OUTPUTS</span></span>

### <span data-ttu-id="7d465-124">Microsoft. Azure. Management. Migration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="7d465-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="7d465-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d465-125">NOTES</span></span>

## <span data-ttu-id="7d465-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d465-126">RELATED LINKS</span></span>
