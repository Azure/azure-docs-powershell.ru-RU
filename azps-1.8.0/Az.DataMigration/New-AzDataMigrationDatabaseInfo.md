---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: f1feead56c25b76890edd0fe183e65211294cf87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731037"
---
# <span data-ttu-id="139e9-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="139e9-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="139e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="139e9-102">SYNOPSIS</span></span>
<span data-ttu-id="139e9-103">Создает объект DatabaseInfo для службы миграции баз данных Azure, указывающий источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="139e9-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="139e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="139e9-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="139e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="139e9-105">DESCRIPTION</span></span>
<span data-ttu-id="139e9-106">Командлет New-AzDataMigrationDatabaseInfo создает объект DatabaseInfo, указывающий экземпляр исходной базы данных, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="139e9-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="139e9-107">Имя базы данных берется из входного параметра.</span><span class="sxs-lookup"><span data-stu-id="139e9-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="139e9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="139e9-108">EXAMPLES</span></span>

### <span data-ttu-id="139e9-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="139e9-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="139e9-110">В предыдущем примере создается новый объект DatabaseInfo для **AdventureWorks2016** исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="139e9-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="139e9-111">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="139e9-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="139e9-112">Вы можете подтвердить свое состояние входа с помощью командлета Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="139e9-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="139e9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="139e9-113">PARAMETERS</span></span>

### <span data-ttu-id="139e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139e9-114">-DefaultProfile</span></span>
<span data-ttu-id="139e9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="139e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="139e9-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="139e9-116">-SourceDatabaseName</span></span>
<span data-ttu-id="139e9-117">Имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="139e9-117">Source Database Name.</span></span>

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

### <span data-ttu-id="139e9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139e9-118">CommonParameters</span></span>
<span data-ttu-id="139e9-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="139e9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139e9-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="139e9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139e9-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="139e9-121">INPUTS</span></span>

### <span data-ttu-id="139e9-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="139e9-122">None</span></span>

## <span data-ttu-id="139e9-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="139e9-123">OUTPUTS</span></span>

### <span data-ttu-id="139e9-124">Microsoft. Azure. Management. Migration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="139e9-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="139e9-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="139e9-125">NOTES</span></span>

## <span data-ttu-id="139e9-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="139e9-126">RELATED LINKS</span></span>
