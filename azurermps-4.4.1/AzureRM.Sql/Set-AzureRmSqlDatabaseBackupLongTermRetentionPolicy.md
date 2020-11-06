---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565108"
---
# <span data-ttu-id="87f3e-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="87f3e-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="87f3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="87f3e-103">Настройка политики хранения для серверной долгосрочной настройки.</span><span class="sxs-lookup"><span data-stu-id="87f3e-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87f3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87f3e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87f3e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="87f3e-106">Командлет **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** задает политику долгосрочного хранения, зарегистрированную для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="87f3e-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="87f3e-107">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="87f3e-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="87f3e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87f3e-108">EXAMPLES</span></span>

## <span data-ttu-id="87f3e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87f3e-109">PARAMETERS</span></span>

### <span data-ttu-id="87f3e-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="87f3e-110">-DatabaseName</span></span>
<span data-ttu-id="87f3e-111">Указывает имя базы данных SQL, для которой этот командлет задает политику.</span><span class="sxs-lookup"><span data-stu-id="87f3e-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="87f3e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f3e-112">-ResourceGroupName</span></span>
<span data-ttu-id="87f3e-113">Указывает имя группы ресурсов, содержащей базу данных.</span><span class="sxs-lookup"><span data-stu-id="87f3e-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="87f3e-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87f3e-114">-ResourceId</span></span>
<span data-ttu-id="87f3e-115">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="87f3e-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f3e-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="87f3e-116">-ServerName</span></span>
<span data-ttu-id="87f3e-117">Указывает сервер, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="87f3e-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="87f3e-118">-State</span><span class="sxs-lookup"><span data-stu-id="87f3e-118">-State</span></span>
<span data-ttu-id="87f3e-119">Задает состояние.</span><span class="sxs-lookup"><span data-stu-id="87f3e-119">Specifies a state.</span></span>

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

### <span data-ttu-id="87f3e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87f3e-120">-Confirm</span></span>
<span data-ttu-id="87f3e-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87f3e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87f3e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87f3e-122">-WhatIf</span></span>
<span data-ttu-id="87f3e-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87f3e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87f3e-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87f3e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87f3e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f3e-125">-DefaultProfile</span></span>
<span data-ttu-id="87f3e-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87f3e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f3e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f3e-127">CommonParameters</span></span>
<span data-ttu-id="87f3e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87f3e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f3e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f3e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f3e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87f3e-130">INPUTS</span></span>

## <span data-ttu-id="87f3e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87f3e-131">OUTPUTS</span></span>

## <span data-ttu-id="87f3e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="87f3e-132">NOTES</span></span>

## <span data-ttu-id="87f3e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87f3e-133">RELATED LINKS</span></span>

[<span data-ttu-id="87f3e-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="87f3e-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="87f3e-135">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="87f3e-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
