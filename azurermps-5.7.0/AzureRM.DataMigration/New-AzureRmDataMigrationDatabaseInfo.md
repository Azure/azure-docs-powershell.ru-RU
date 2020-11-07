---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734459"
---
# <span data-ttu-id="7465b-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="7465b-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="7465b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7465b-102">SYNOPSIS</span></span>
<span data-ttu-id="7465b-103">Создает объект DatabaseInfo для службы миграции баз данных Azure, указывающий источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="7465b-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7465b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7465b-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="7465b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7465b-105">DESCRIPTION</span></span>
<span data-ttu-id="7465b-106">Командлет New-AzureRmDataMigrationDatabaseInfo создает объект DatabaseInfo, указывающий экземпляр исходной базы данных, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="7465b-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="7465b-107">Имя базы данных берется из входного параметра.</span><span class="sxs-lookup"><span data-stu-id="7465b-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="7465b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7465b-108">EXAMPLES</span></span>

### <span data-ttu-id="7465b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7465b-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="7465b-110">В предыдущем примере создается новый объект DatabaseInfo для **AdventureWorks2016** исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7465b-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="7465b-111">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7465b-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="7465b-112">Вы можете подтвердить свое состояние входа с помощью командлета Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="7465b-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="7465b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7465b-113">PARAMETERS</span></span>

### <span data-ttu-id="7465b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7465b-114">-DefaultProfile</span></span>
<span data-ttu-id="7465b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7465b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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
### <span data-ttu-id="7465b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7465b-116">-Confirm</span></span>
<span data-ttu-id="7465b-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7465b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7465b-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7465b-118">-SourceDatabaseName</span></span>
<span data-ttu-id="7465b-119">Имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="7465b-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7465b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7465b-120">-WhatIf</span></span>
<span data-ttu-id="7465b-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7465b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7465b-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7465b-122">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="7465b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7465b-123">INPUTS</span></span>

### <span data-ttu-id="7465b-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="7465b-124">None</span></span>


## <span data-ttu-id="7465b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7465b-125">OUTPUTS</span></span>

### <span data-ttu-id="7465b-126">Microsoft. Azure. Management. Migration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="7465b-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="7465b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="7465b-127">NOTES</span></span>

## <span data-ttu-id="7465b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7465b-128">RELATED LINKS</span></span>


