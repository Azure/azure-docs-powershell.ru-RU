---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065386"
---
# <span data-ttu-id="2bedf-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="2bedf-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="2bedf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bedf-102">SYNOPSIS</span></span>
<span data-ttu-id="2bedf-103">Создает объект общего файлового обмена для службы миграции баз данных Azure, который определяет локальную общую сетевую папке, в которую нужно сделать резервные копии исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="2bedf-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="2bedf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bedf-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bedf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bedf-105">DESCRIPTION</span></span>
<span data-ttu-id="2bedf-106">Командлет New-AzDataMigrationFileShare создает объект общего доступа, указывающий локальную сетевую общую сеть, в которую служба миграции баз данных Azure может создавать резервные копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="2bedf-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="2bedf-107">У учетной записи службы исходного экземпляра SQL Server должны быть права на запись в этой сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="2bedf-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="2bedf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bedf-108">EXAMPLES</span></span>

### <span data-ttu-id="2bedf-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bedf-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="2bedf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bedf-110">PARAMETERS</span></span>

### <span data-ttu-id="2bedf-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="2bedf-111">-Credential</span></span>
<span data-ttu-id="2bedf-112">Учетные данные для доступа к общему файловому ресурсам.</span><span class="sxs-lookup"><span data-stu-id="2bedf-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="2bedf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bedf-113">-DefaultProfile</span></span>
<span data-ttu-id="2bedf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bedf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bedf-115">-Path</span><span class="sxs-lookup"><span data-stu-id="2bedf-115">-Path</span></span>
<span data-ttu-id="2bedf-116">Путь к общему файловому файлу.</span><span class="sxs-lookup"><span data-stu-id="2bedf-116">File share path.</span></span>

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

### <span data-ttu-id="2bedf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bedf-117">CommonParameters</span></span>
<span data-ttu-id="2bedf-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bedf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bedf-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bedf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bedf-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bedf-120">INPUTS</span></span>

### <span data-ttu-id="2bedf-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="2bedf-121">None</span></span>

## <span data-ttu-id="2bedf-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bedf-122">OUTPUTS</span></span>

### <span data-ttu-id="2bedf-123">Microsoft. Azure. Management. Migration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="2bedf-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="2bedf-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bedf-124">NOTES</span></span>

## <span data-ttu-id="2bedf-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bedf-125">RELATED LINKS</span></span>
