---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 85dc7d386dc64f8c384f9aae7925379375b95a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562015"
---
# <span data-ttu-id="729a1-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="729a1-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="729a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="729a1-102">SYNOPSIS</span></span>
<span data-ttu-id="729a1-103">Переключается на базу данных-получатель в качестве основной, чтобы начать переход на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="729a1-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="729a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="729a1-104">SYNTAX</span></span>

### <span data-ttu-id="729a1-105">Параметр "нестандартные" (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="729a1-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729a1-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="729a1-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="729a1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="729a1-107">DESCRIPTION</span></span>
<span data-ttu-id="729a1-108">Командлет **Set-AzureRmSqlDatabaseSecondary** переключает вторичную базу данных в первичную для инициирования отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="729a1-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="729a1-109">Этот командлет разработан как общая команда конфигурации, но в настоящее время она ограничена запуском отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="729a1-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="729a1-110">Укажите параметр *AllowDataLoss* для инициирования принудительной отработки отказа во время сбоя.</span><span class="sxs-lookup"><span data-stu-id="729a1-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="729a1-111">Вам не нужно указывать этот параметр при выполнении запланированной операции, например детализации для восстановления.</span><span class="sxs-lookup"><span data-stu-id="729a1-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="729a1-112">В последнем случае база данных получателя синхронизируется с основным приложением перед тем, как он будет переключен.</span><span class="sxs-lookup"><span data-stu-id="729a1-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="729a1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="729a1-113">EXAMPLES</span></span>

## <span data-ttu-id="729a1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="729a1-114">PARAMETERS</span></span>

### <span data-ttu-id="729a1-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="729a1-115">-AllowDataLoss</span></span>
<span data-ttu-id="729a1-116">Указывает на то, что эта операция отработки отказа позволяет избежать потери данных.</span><span class="sxs-lookup"><span data-stu-id="729a1-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="729a1-117">-DatabaseName</span></span>
<span data-ttu-id="729a1-118">Указывает имя вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="729a1-118">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729a1-119">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="729a1-119">-Failover</span></span>
<span data-ttu-id="729a1-120">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="729a1-120">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a1-121">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729a1-121">-PartnerResourceGroupName</span></span>
<span data-ttu-id="729a1-122">Указывает имя группы ресурсов, которой назначена база данных SQL партнера Azure.</span><span class="sxs-lookup"><span data-stu-id="729a1-122">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="729a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="729a1-124">Указывает имя группы ресурсов, которой назначена служба вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="729a1-124">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="729a1-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="729a1-125">-ServerName</span></span>
<span data-ttu-id="729a1-126">Указывает имя сервера SQL Server, на котором размещена дополнительная база данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="729a1-126">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729a1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="729a1-127">-Confirm</span></span>
<span data-ttu-id="729a1-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="729a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729a1-129">-WhatIf</span></span>
<span data-ttu-id="729a1-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="729a1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="729a1-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="729a1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729a1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729a1-132">-DefaultProfile</span></span>
<span data-ttu-id="729a1-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="729a1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="729a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729a1-134">CommonParameters</span></span>
<span data-ttu-id="729a1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="729a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729a1-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="729a1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729a1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="729a1-137">INPUTS</span></span>

###  
<span data-ttu-id="729a1-138">Вы можете создать канал для экземпляра объекта **базы данных** для базы данных получателя, чтобы выполнить переход на другой элемент, а затем сделать его базой данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="729a1-138">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="729a1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="729a1-139">OUTPUTS</span></span>

###  
<span data-ttu-id="729a1-140">Этот командлет возвращает объект **ReplicationLink**.</span><span class="sxs-lookup"><span data-stu-id="729a1-140">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="729a1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="729a1-141">NOTES</span></span>

## <span data-ttu-id="729a1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="729a1-142">RELATED LINKS</span></span>

[<span data-ttu-id="729a1-143">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="729a1-143">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="729a1-144">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="729a1-144">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="729a1-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="729a1-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
