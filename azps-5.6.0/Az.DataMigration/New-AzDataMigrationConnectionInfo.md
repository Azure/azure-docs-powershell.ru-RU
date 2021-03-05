---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: cfd8df9bc329ef252c28ef826b1ba68a1946bab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966632"
---
# <span data-ttu-id="d6b16-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d6b16-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="d6b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b16-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b16-103">Создание объекта "Сведения о под соединении", определяющий тип сервера и имя подключения.</span><span class="sxs-lookup"><span data-stu-id="d6b16-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="d6b16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6b16-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6b16-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6b16-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b16-106">С New-AzDataMigrationConnectionInfo создается объект Connection Info, определяющий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="d6b16-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="d6b16-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6b16-107">EXAMPLES</span></span>

### <span data-ttu-id="d6b16-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6b16-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="d6b16-109">В предыдущем примере создается объект Connection Info, который SQL в качестве параметра ServerType.</span><span class="sxs-lookup"><span data-stu-id="d6b16-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="d6b16-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6b16-110">PARAMETERS</span></span>

### <span data-ttu-id="d6b16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b16-111">-DefaultProfile</span></span>
<span data-ttu-id="d6b16-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6b16-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="d6b16-113">-ServerType</span></span>
<span data-ttu-id="d6b16-114">Enum that describes server type to connect to.</span><span class="sxs-lookup"><span data-stu-id="d6b16-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="d6b16-115">В настоящее время поддерживаются значения SQL для SQL Server, azure SQL Managed Instance, MongoDb, Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d6b16-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b16-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b16-116">CommonParameters</span></span>
<span data-ttu-id="d6b16-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b16-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b16-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b16-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b16-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6b16-119">INPUTS</span></span>

### <span data-ttu-id="d6b16-120">Нет</span><span class="sxs-lookup"><span data-stu-id="d6b16-120">None</span></span>

## <span data-ttu-id="d6b16-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6b16-121">OUTPUTS</span></span>

### <span data-ttu-id="d6b16-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d6b16-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="d6b16-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6b16-123">NOTES</span></span>

## <span data-ttu-id="d6b16-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6b16-124">RELATED LINKS</span></span>
