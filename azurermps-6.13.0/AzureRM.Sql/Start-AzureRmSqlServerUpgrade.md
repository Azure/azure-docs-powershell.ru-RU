---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562527"
---
# <span data-ttu-id="64687-101">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="64687-101">Start-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="64687-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64687-102">SYNOPSIS</span></span>
<span data-ttu-id="64687-103">Запускает обновление сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="64687-103">Starts the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64687-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64687-104">SYNTAX</span></span>

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64687-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64687-105">DESCRIPTION</span></span>
<span data-ttu-id="64687-106">Командлет **Start-AzureRmSqlServerUpgrade** запускает обновление сервера базы данных SQL Azure версии 11 до версии 12.</span><span class="sxs-lookup"><span data-stu-id="64687-106">The **Start-AzureRmSqlServerUpgrade** cmdlet starts the upgrade of an Azure SQL Database server version 11 to version 12.</span></span>
<span data-ttu-id="64687-107">Вы можете отслеживать ход выполнения обновления с помощью командлета Get-AzureRmSqlServerUpgrade.</span><span class="sxs-lookup"><span data-stu-id="64687-107">You can monitor the progress of an upgrade by using the Get-AzureRmSqlServerUpgrade cmdlet.</span></span>

## <span data-ttu-id="64687-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64687-108">EXAMPLES</span></span>

### <span data-ttu-id="64687-109">Пример 1: обновление сервера</span><span class="sxs-lookup"><span data-stu-id="64687-109">Example 1: Upgrade a server</span></span>
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

<span data-ttu-id="64687-110">Эта команда обновляет сервер с именем Server01, назначенный группе ресурсов TesourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="64687-110">This command upgrades the server named server01 assigned to resource group TesourceGroup01.</span></span>

### <span data-ttu-id="64687-111">Пример 2: обновление сервера с помощью расписания и рекомендации по базе данных</span><span class="sxs-lookup"><span data-stu-id="64687-111">Example 2: Upgrade a server by using schedule time and database recommendation</span></span>
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

<span data-ttu-id="64687-112">Первая команда создает время на пять минут в будущем с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="64687-112">The first command creates a time five minutes in the future by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="64687-113">Эта команда хранит дату в $ScheduleTime переменной.</span><span class="sxs-lookup"><span data-stu-id="64687-113">The command stores the date in the variable $ScheduleTime.</span></span>
<span data-ttu-id="64687-114">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="64687-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="64687-115">Вторая команда создает объект **RecommendedDatabaseProperties** , а затем сохраняет этот объект в переменной $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="64687-115">The second command creates a **RecommendedDatabaseProperties** object, and then stores that object in the variable $DatabaseMap.</span></span>
<span data-ttu-id="64687-116">Следующие три команды назначают значения свойствам объекта, хранящегося в $DatabaseMap.</span><span class="sxs-lookup"><span data-stu-id="64687-116">The next three commands assign values to properties of the object stored in $DatabaseMap.</span></span>
<span data-ttu-id="64687-117">Последняя команда обновляет существующий сервер с именем Server01 и версией 12,0.</span><span class="sxs-lookup"><span data-stu-id="64687-117">The final command upgrades the existing server named Server01 to version 12.0.</span></span>
<span data-ttu-id="64687-118">Самое раннее время обновления — это пять минут после выполнения команды, как указано в переменной $ScheduleTime.</span><span class="sxs-lookup"><span data-stu-id="64687-118">The earliest time to upgrade is five minutes after you run the command, as specified by the $ScheduleTime variable.</span></span>
<span data-ttu-id="64687-119">После обновления ContosoDB базы данных будет работать в стандартном выпуске и иметь уровень обслуживания объектив S0.</span><span class="sxs-lookup"><span data-stu-id="64687-119">After the upgrade, the database contosodb will be running the Standard edition and have the Service Level Objective S0.</span></span>

## <span data-ttu-id="64687-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64687-120">PARAMETERS</span></span>

### <span data-ttu-id="64687-121">-DatabaseCollection</span><span class="sxs-lookup"><span data-stu-id="64687-121">-DatabaseCollection</span></span>
<span data-ttu-id="64687-122">Задает массив объектов **RecommendedDatabaseProperties** , используемых этим командлетом для обновления сервера.</span><span class="sxs-lookup"><span data-stu-id="64687-122">Specifies an array of **RecommendedDatabaseProperties** objects that this cmdlet uses for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64687-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64687-123">-DefaultProfile</span></span>
<span data-ttu-id="64687-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="64687-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64687-125">-ElasticPoolCollection</span><span class="sxs-lookup"><span data-stu-id="64687-125">-ElasticPoolCollection</span></span>
<span data-ttu-id="64687-126">Задает массив объектов **UpgradeRecommendedElasticPoolProperties** , которые нужно использовать для обновления сервера.</span><span class="sxs-lookup"><span data-stu-id="64687-126">Specifies an array of **UpgradeRecommendedElasticPoolProperties** objects to use for the server upgrade.</span></span>

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64687-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64687-127">-ResourceGroupName</span></span>
<span data-ttu-id="64687-128">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="64687-128">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64687-129">-ScheduleUpgradeAfterUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="64687-129">-ScheduleUpgradeAfterUtcDateTime</span></span>
<span data-ttu-id="64687-130">Задает самое раннее время в качестве объекта **DateTime** , чтобы обновить сервер.</span><span class="sxs-lookup"><span data-stu-id="64687-130">Specifies the earliest time, as a **DateTime** object, to upgrade the server.</span></span>
<span data-ttu-id="64687-131">Укажите значение в формате ISO8601 в всеобщем скоординированном времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="64687-131">Specify a value in the ISO8601 format, in Coordinated Universal Time (UTC).</span></span>
<span data-ttu-id="64687-132">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="64687-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64687-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="64687-133">-ServerName</span></span>
<span data-ttu-id="64687-134">Указывает имя сервера, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="64687-134">Specifies the name of the server that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64687-135">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="64687-135">-ServerVersion</span></span>
<span data-ttu-id="64687-136">Указывает версию, на которую этот командлет обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="64687-136">Specifies the version to which this cmdlet upgrades the server.</span></span>
<span data-ttu-id="64687-137">Единственным допустимым значением является 12,0.</span><span class="sxs-lookup"><span data-stu-id="64687-137">The only valid value is 12.0.</span></span>

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

### <span data-ttu-id="64687-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64687-138">CommonParameters</span></span>
<span data-ttu-id="64687-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64687-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64687-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64687-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64687-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64687-141">INPUTS</span></span>

### <span data-ttu-id="64687-142">System. String</span><span class="sxs-lookup"><span data-stu-id="64687-142">System.String</span></span>

## <span data-ttu-id="64687-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64687-143">OUTPUTS</span></span>

### <span data-ttu-id="64687-144">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeStartModel</span><span class="sxs-lookup"><span data-stu-id="64687-144">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeStartModel</span></span>

## <span data-ttu-id="64687-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="64687-145">NOTES</span></span>

## <span data-ttu-id="64687-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64687-146">RELATED LINKS</span></span>

[<span data-ttu-id="64687-147">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="64687-147">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="64687-148">Остановить-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="64687-148">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="64687-149">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="64687-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


