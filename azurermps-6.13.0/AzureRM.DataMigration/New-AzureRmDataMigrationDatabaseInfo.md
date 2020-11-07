---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734968"
---
# <span data-ttu-id="f72b4-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f72b4-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="f72b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f72b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f72b4-103">Создает объект DatabaseInfo для службы миграции баз данных Azure, указывающий источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="f72b4-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f72b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f72b4-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f72b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f72b4-105">DESCRIPTION</span></span>
<span data-ttu-id="f72b4-106">Командлет New-AzureRmDataMigrationDatabaseInfo создает объект DatabaseInfo, указывающий экземпляр исходной базы данных, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="f72b4-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="f72b4-107">Имя базы данных берется из входного параметра.</span><span class="sxs-lookup"><span data-stu-id="f72b4-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="f72b4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f72b4-108">EXAMPLES</span></span>

### <span data-ttu-id="f72b4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f72b4-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="f72b4-110">В предыдущем примере создается новый объект DatabaseInfo для **AdventureWorks2016** исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="f72b4-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="f72b4-111">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="f72b4-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="f72b4-112">Вы можете подтвердить свое состояние входа с помощью командлета Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="f72b4-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="f72b4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f72b4-113">PARAMETERS</span></span>

### <span data-ttu-id="f72b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72b4-114">-DefaultProfile</span></span>
<span data-ttu-id="f72b4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f72b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f72b4-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f72b4-116">-SourceDatabaseName</span></span>
<span data-ttu-id="f72b4-117">Имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="f72b4-117">Source Database Name.</span></span>

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

### <span data-ttu-id="f72b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72b4-118">CommonParameters</span></span>
<span data-ttu-id="f72b4-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f72b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72b4-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f72b4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72b4-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f72b4-121">INPUTS</span></span>

### <span data-ttu-id="f72b4-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="f72b4-122">None</span></span>

## <span data-ttu-id="f72b4-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f72b4-123">OUTPUTS</span></span>

### <span data-ttu-id="f72b4-124">Microsoft. Azure. Management. Migration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f72b4-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="f72b4-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f72b4-125">NOTES</span></span>

## <span data-ttu-id="f72b4-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f72b4-126">RELATED LINKS</span></span>
