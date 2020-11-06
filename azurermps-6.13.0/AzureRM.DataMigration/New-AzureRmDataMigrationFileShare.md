---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567761"
---
# <span data-ttu-id="65ac8-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="65ac8-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="65ac8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="65ac8-103">Создает объект общего файлового обмена для службы миграции баз данных Azure, который определяет локальную общую сетевую папке, в которую нужно сделать резервные копии исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="65ac8-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ac8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65ac8-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ac8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="65ac8-106">Командлет New-AzureRmDataMigrationFileShare создает объект общего доступа, указывающий локальную сетевую общую сеть, в которую служба миграции баз данных Azure может создавать резервные копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="65ac8-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="65ac8-107">У учетной записи службы исходного экземпляра SQL Server должны быть права на запись в этой сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="65ac8-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="65ac8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65ac8-108">EXAMPLES</span></span>

### <span data-ttu-id="65ac8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65ac8-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="65ac8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65ac8-110">PARAMETERS</span></span>

### <span data-ttu-id="65ac8-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="65ac8-111">-Credential</span></span>
<span data-ttu-id="65ac8-112">Учетные данные для доступа к общему файловому ресурсам.</span><span class="sxs-lookup"><span data-stu-id="65ac8-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="65ac8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ac8-113">-DefaultProfile</span></span>
<span data-ttu-id="65ac8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65ac8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65ac8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="65ac8-115">-Path</span></span>
<span data-ttu-id="65ac8-116">Путь к общему файловому файлу.</span><span class="sxs-lookup"><span data-stu-id="65ac8-116">File share path.</span></span>

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

### <span data-ttu-id="65ac8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ac8-117">CommonParameters</span></span>
<span data-ttu-id="65ac8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65ac8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ac8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ac8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ac8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65ac8-120">INPUTS</span></span>

### <span data-ttu-id="65ac8-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="65ac8-121">None</span></span>

## <span data-ttu-id="65ac8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65ac8-122">OUTPUTS</span></span>

### <span data-ttu-id="65ac8-123">Microsoft. Azure. Management. Migration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="65ac8-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="65ac8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="65ac8-124">NOTES</span></span>

## <span data-ttu-id="65ac8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65ac8-125">RELATED LINKS</span></span>
