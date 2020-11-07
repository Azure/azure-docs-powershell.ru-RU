---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c9940f5278390fc72dbd8e7d906718f01375583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734207"
---
# <span data-ttu-id="5ad12-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="5ad12-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="5ad12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ad12-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad12-103">Прекращение обновления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5ad12-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ad12-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ad12-105">DESCRIPTION</span></span>
<span data-ttu-id="5ad12-106">Командлет **Stop-AzureRmSqlServerUpgrade** останавливает обновление сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad12-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="5ad12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ad12-107">EXAMPLES</span></span>

### <span data-ttu-id="5ad12-108">Пример 1: остановка обновления сервера</span><span class="sxs-lookup"><span data-stu-id="5ad12-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="5ad12-109">Эта команда останавливает запрос на обновление сервера с именем SERVER02, назначенного группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5ad12-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="5ad12-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ad12-110">PARAMETERS</span></span>

### <span data-ttu-id="5ad12-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5ad12-111">-Force</span></span>
<span data-ttu-id="5ad12-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ad12-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad12-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad12-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ad12-114">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="5ad12-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5ad12-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5ad12-115">-ServerName</span></span>
<span data-ttu-id="5ad12-116">Указывает имя сервера, для которого этот командлет останавливает обновление.</span><span class="sxs-lookup"><span data-stu-id="5ad12-116">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="5ad12-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ad12-117">-Confirm</span></span>
<span data-ttu-id="5ad12-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ad12-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ad12-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad12-119">-WhatIf</span></span>
<span data-ttu-id="5ad12-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ad12-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ad12-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ad12-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ad12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad12-122">-DefaultProfile</span></span>
<span data-ttu-id="5ad12-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad12-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ad12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad12-124">CommonParameters</span></span>
<span data-ttu-id="5ad12-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ad12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad12-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad12-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad12-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ad12-127">INPUTS</span></span>

### <span data-ttu-id="5ad12-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="5ad12-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="5ad12-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ad12-129">OUTPUTS</span></span>

## <span data-ttu-id="5ad12-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ad12-130">NOTES</span></span>

## <span data-ttu-id="5ad12-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ad12-131">RELATED LINKS</span></span>

[<span data-ttu-id="5ad12-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="5ad12-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="5ad12-133">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="5ad12-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="5ad12-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5ad12-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


