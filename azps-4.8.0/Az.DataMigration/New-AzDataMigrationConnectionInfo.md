---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236756"
---
# <span data-ttu-id="28556-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="28556-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="28556-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28556-102">SYNOPSIS</span></span>
<span data-ttu-id="28556-103">Создает новый объект сведений о соединении, указывающий тип сервера и имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="28556-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="28556-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28556-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28556-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28556-105">DESCRIPTION</span></span>
<span data-ttu-id="28556-106">Командлет New-AzDataMigrationConnectionInfo создает новый объект сведений о соединении, указывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="28556-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="28556-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28556-107">EXAMPLES</span></span>

### <span data-ttu-id="28556-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28556-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="28556-109">В предыдущем примере создается объект сведений о соединении, предоставляющий SQL AS для параметра ServerType.</span><span class="sxs-lookup"><span data-stu-id="28556-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="28556-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28556-110">PARAMETERS</span></span>

### <span data-ttu-id="28556-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28556-111">-DefaultProfile</span></span>
<span data-ttu-id="28556-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28556-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28556-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="28556-113">-ServerType</span></span>
<span data-ttu-id="28556-114">Enum, описывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="28556-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="28556-115">В настоящее время поддерживаются значения SQL Server, управляемый экземпляр Azure SQL, MongoDb, CosmosDb и Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="28556-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="28556-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28556-116">CommonParameters</span></span>
<span data-ttu-id="28556-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28556-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28556-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28556-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28556-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28556-119">INPUTS</span></span>

### <span data-ttu-id="28556-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="28556-120">None</span></span>

## <span data-ttu-id="28556-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28556-121">OUTPUTS</span></span>

### <span data-ttu-id="28556-122">Microsoft. Azure. Management. Migration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="28556-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="28556-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="28556-123">NOTES</span></span>

## <span data-ttu-id="28556-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28556-124">RELATED LINKS</span></span>