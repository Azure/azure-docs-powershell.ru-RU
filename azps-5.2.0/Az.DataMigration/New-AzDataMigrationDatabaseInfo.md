---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327658"
---
# <span data-ttu-id="a4450-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="a4450-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="a4450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4450-102">SYNOPSIS</span></span>
<span data-ttu-id="a4450-103">Создание объекта DatabaseInfo для службы миграции баз данных Azure, которая определяет источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="a4450-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="a4450-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4450-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4450-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4450-105">DESCRIPTION</span></span>
<span data-ttu-id="a4450-106">С New-AzDataMigrationDatabaseInfo создается объект DatabaseInfo, который определяет переносимый экземпляр базы данных.</span><span class="sxs-lookup"><span data-stu-id="a4450-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="a4450-107">Имя базы данных в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="a4450-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="a4450-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4450-108">EXAMPLES</span></span>

### <span data-ttu-id="a4450-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4450-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="a4450-110">В предыдущем примере создается объект DatabaseInfo для базы **данных AdventureWorks2016.**</span><span class="sxs-lookup"><span data-stu-id="a4450-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="a4450-111">Предполагается, что вы уже вошли в свою учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="a4450-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="a4450-112">Вы можете подтвердить состояние входа с помощью Get-AzSubscription управления.</span><span class="sxs-lookup"><span data-stu-id="a4450-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="a4450-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4450-113">PARAMETERS</span></span>

### <span data-ttu-id="a4450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4450-114">-DefaultProfile</span></span>
<span data-ttu-id="a4450-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4450-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4450-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4450-116">-SourceDatabaseName</span></span>
<span data-ttu-id="a4450-117">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="a4450-117">Source Database Name.</span></span>

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

### <span data-ttu-id="a4450-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4450-118">CommonParameters</span></span>
<span data-ttu-id="a4450-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4450-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4450-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4450-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4450-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4450-121">INPUTS</span></span>

### <span data-ttu-id="a4450-122">Нет</span><span class="sxs-lookup"><span data-stu-id="a4450-122">None</span></span>

## <span data-ttu-id="a4450-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4450-123">OUTPUTS</span></span>

### <span data-ttu-id="a4450-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="a4450-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="a4450-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4450-125">NOTES</span></span>

## <span data-ttu-id="a4450-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4450-126">RELATED LINKS</span></span>
