---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732952"
---
# <span data-ttu-id="2938d-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2938d-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="2938d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2938d-102">SYNOPSIS</span></span>
<span data-ttu-id="2938d-103">Создает новый объект сведений о соединении, указывающий тип сервера и имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="2938d-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2938d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2938d-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2938d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2938d-105">DESCRIPTION</span></span>
<span data-ttu-id="2938d-106">Командлет New-AzureRmDataMigrationConnectionInfo создает новый объект сведений о соединении, указывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="2938d-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="2938d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2938d-107">EXAMPLES</span></span>

### <span data-ttu-id="2938d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2938d-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="2938d-109">В предыдущем примере создается объект сведений о соединении, предоставляющий SQL AS для параметра ServerType.</span><span class="sxs-lookup"><span data-stu-id="2938d-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="2938d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2938d-110">PARAMETERS</span></span>

### <span data-ttu-id="2938d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2938d-111">-DefaultProfile</span></span>
<span data-ttu-id="2938d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2938d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2938d-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="2938d-113">-ServerType</span></span>
<span data-ttu-id="2938d-114">Enum, описывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="2938d-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="2938d-115">В настоящее время поддерживаются значения SQL Server, управляемый экземпляр SQL Server Azure и база данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2938d-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2938d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2938d-116">CommonParameters</span></span>
<span data-ttu-id="2938d-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2938d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2938d-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2938d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2938d-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2938d-119">INPUTS</span></span>

### <span data-ttu-id="2938d-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="2938d-120">None</span></span>

## <span data-ttu-id="2938d-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2938d-121">OUTPUTS</span></span>

### <span data-ttu-id="2938d-122">Microsoft. Azure. Management. Migration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2938d-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="2938d-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="2938d-123">NOTES</span></span>

## <span data-ttu-id="2938d-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2938d-124">RELATED LINKS</span></span>
