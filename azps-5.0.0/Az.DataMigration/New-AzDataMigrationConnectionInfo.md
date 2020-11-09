---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313166"
---
# <span data-ttu-id="edc6c-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="edc6c-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="edc6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="edc6c-103">Создает новый объект сведений о соединении, указывающий тип сервера и имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="edc6c-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="edc6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edc6c-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edc6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edc6c-105">DESCRIPTION</span></span>
<span data-ttu-id="edc6c-106">Командлет New-AzDataMigrationConnectionInfo создает новый объект сведений о соединении, указывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="edc6c-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="edc6c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edc6c-107">EXAMPLES</span></span>

### <span data-ttu-id="edc6c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edc6c-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="edc6c-109">В предыдущем примере создается объект сведений о соединении, предоставляющий SQL AS для параметра ServerType.</span><span class="sxs-lookup"><span data-stu-id="edc6c-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="edc6c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edc6c-110">PARAMETERS</span></span>

### <span data-ttu-id="edc6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc6c-111">-DefaultProfile</span></span>
<span data-ttu-id="edc6c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edc6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edc6c-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="edc6c-113">-ServerType</span></span>
<span data-ttu-id="edc6c-114">Enum, описывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="edc6c-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="edc6c-115">В настоящее время поддерживаются значения SQL Server, управляемый экземпляр Azure SQL, MongoDb, CosmosDb и Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="edc6c-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="edc6c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc6c-116">CommonParameters</span></span>
<span data-ttu-id="edc6c-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edc6c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc6c-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc6c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc6c-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edc6c-119">INPUTS</span></span>

### <span data-ttu-id="edc6c-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="edc6c-120">None</span></span>

## <span data-ttu-id="edc6c-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edc6c-121">OUTPUTS</span></span>

### <span data-ttu-id="edc6c-122">Microsoft. Azure. Management. Migration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="edc6c-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="edc6c-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="edc6c-123">NOTES</span></span>

## <span data-ttu-id="edc6c-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edc6c-124">RELATED LINKS</span></span>
