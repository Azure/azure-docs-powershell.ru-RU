---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560383"
---
# <span data-ttu-id="091db-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="091db-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="091db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="091db-102">SYNOPSIS</span></span>
<span data-ttu-id="091db-103">Создает новый объект сведений о соединении, указывающий тип сервера и имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="091db-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="091db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="091db-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="091db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="091db-105">DESCRIPTION</span></span>
<span data-ttu-id="091db-106">Командлет New-AzureRmDataMigrationConnectionInfo создает новый объект сведений о соединении, указывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="091db-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="091db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="091db-107">EXAMPLES</span></span>

### <span data-ttu-id="091db-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="091db-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="091db-109">В предыдущем примере создается объект сведений о соединении, предоставляющий SQL AS для параметра ServerType.</span><span class="sxs-lookup"><span data-stu-id="091db-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="091db-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="091db-110">PARAMETERS</span></span>

### <span data-ttu-id="091db-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="091db-111">-Confirm</span></span>
<span data-ttu-id="091db-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="091db-112">Prompts you for confirmation before running the cmdlet.</span></span>

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
### <span data-ttu-id="091db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091db-113">-DefaultProfile</span></span>
<span data-ttu-id="091db-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="091db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="091db-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="091db-115">-ServerType</span></span>
<span data-ttu-id="091db-116">Enum, описывающий тип сервера для подключения.</span><span class="sxs-lookup"><span data-stu-id="091db-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="091db-117">В настоящее время поддерживаются значения SQL для SQL Server и SQLDB для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="091db-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="091db-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="091db-118">-AuthType</span></span>
<span data-ttu-id="091db-119">Тип проверки подлинности, который будет использоваться для подключения.</span><span class="sxs-lookup"><span data-stu-id="091db-119">Authentication type to use for connection.</span></span> <span data-ttu-id="091db-120">Возможные значения — SqlAuthentication и WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="091db-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091db-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="091db-121">-DataSource</span></span>
<span data-ttu-id="091db-122">Сервер address\name, к которому нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="091db-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091db-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="091db-123">-TrustServerCertificate</span></span>
<span data-ttu-id="091db-124">Логическое значение, указывающее, что шифрование будет происходить.</span><span class="sxs-lookup"><span data-stu-id="091db-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091db-125">-WhatIf</span></span>
<span data-ttu-id="091db-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="091db-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="091db-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="091db-127">The cmdlet is not run.</span></span>

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





## <span data-ttu-id="091db-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="091db-128">INPUTS</span></span>

### <span data-ttu-id="091db-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="091db-129">None</span></span>


## <span data-ttu-id="091db-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="091db-130">OUTPUTS</span></span>

### <span data-ttu-id="091db-131">Microsoft. Azure. Management. Migration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="091db-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="091db-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="091db-132">NOTES</span></span>

## <span data-ttu-id="091db-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="091db-133">RELATED LINKS</span></span>

