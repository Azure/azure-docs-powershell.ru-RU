---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426535"
---
# <span data-ttu-id="fb436-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="fb436-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="fb436-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb436-102">SYNOPSIS</span></span>
<span data-ttu-id="fb436-103">Создание объекта FileShare для службы миграции баз данных Azure, в которой указывается локализованная сетевая папка, в которую нужно архивации.</span><span class="sxs-lookup"><span data-stu-id="fb436-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="fb436-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb436-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb436-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb436-105">DESCRIPTION</span></span>
<span data-ttu-id="fb436-106">С New-AzDataMigrationFileShare создается объект FileShare, задав локализованную сетевую папку, в которую служба миграции базы данных Azure может использовать резервные копии.</span><span class="sxs-lookup"><span data-stu-id="fb436-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="fb436-107">У учетной записи службы, запущенной SQL Server источника, должны быть права на запись в этой сетевой доли.</span><span class="sxs-lookup"><span data-stu-id="fb436-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="fb436-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb436-108">EXAMPLES</span></span>

### <span data-ttu-id="fb436-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb436-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="fb436-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb436-110">PARAMETERS</span></span>

### <span data-ttu-id="fb436-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="fb436-111">-Credential</span></span>
<span data-ttu-id="fb436-112">Учетные данные для доступа к файловой папке.</span><span class="sxs-lookup"><span data-stu-id="fb436-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb436-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb436-113">-DefaultProfile</span></span>
<span data-ttu-id="fb436-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb436-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb436-115">-Path</span><span class="sxs-lookup"><span data-stu-id="fb436-115">-Path</span></span>
<span data-ttu-id="fb436-116">Путь к файловой папке.</span><span class="sxs-lookup"><span data-stu-id="fb436-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb436-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb436-117">CommonParameters</span></span>
<span data-ttu-id="fb436-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb436-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb436-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb436-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb436-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb436-120">INPUTS</span></span>

### <span data-ttu-id="fb436-121">Нет</span><span class="sxs-lookup"><span data-stu-id="fb436-121">None</span></span>

## <span data-ttu-id="fb436-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb436-122">OUTPUTS</span></span>

### <span data-ttu-id="fb436-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="fb436-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="fb436-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb436-124">NOTES</span></span>

## <span data-ttu-id="fb436-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb436-125">RELATED LINKS</span></span>
