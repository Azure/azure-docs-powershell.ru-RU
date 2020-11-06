---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557032"
---
# <span data-ttu-id="4eafc-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4eafc-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="4eafc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4eafc-102">SYNOPSIS</span></span>
<span data-ttu-id="4eafc-103">Прекращение обновления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="4eafc-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eafc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4eafc-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eafc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eafc-105">DESCRIPTION</span></span>
<span data-ttu-id="4eafc-106">Командлет **Stop-AzureRmSqlServerUpgrade** останавливает обновление сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4eafc-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="4eafc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4eafc-107">EXAMPLES</span></span>

### <span data-ttu-id="4eafc-108">Пример 1: остановка обновления сервера</span><span class="sxs-lookup"><span data-stu-id="4eafc-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="4eafc-109">Эта команда останавливает запрос на обновление сервера с именем SERVER02, назначенного группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4eafc-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4eafc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4eafc-110">PARAMETERS</span></span>

### <span data-ttu-id="4eafc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eafc-111">-DefaultProfile</span></span>
<span data-ttu-id="4eafc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4eafc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eafc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4eafc-113">-Force</span></span>
<span data-ttu-id="4eafc-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4eafc-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eafc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eafc-115">-ResourceGroupName</span></span>
<span data-ttu-id="4eafc-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="4eafc-116">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eafc-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4eafc-117">-ServerName</span></span>
<span data-ttu-id="4eafc-118">Указывает имя сервера, для которого этот командлет останавливает обновление.</span><span class="sxs-lookup"><span data-stu-id="4eafc-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eafc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eafc-119">-Confirm</span></span>
<span data-ttu-id="4eafc-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4eafc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eafc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eafc-121">-WhatIf</span></span>
<span data-ttu-id="4eafc-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4eafc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eafc-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4eafc-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eafc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eafc-124">CommonParameters</span></span>
<span data-ttu-id="4eafc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4eafc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eafc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eafc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eafc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4eafc-127">INPUTS</span></span>

### <span data-ttu-id="4eafc-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="4eafc-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="4eafc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eafc-129">OUTPUTS</span></span>

## <span data-ttu-id="4eafc-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4eafc-130">NOTES</span></span>

## <span data-ttu-id="4eafc-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4eafc-131">RELATED LINKS</span></span>

[<span data-ttu-id="4eafc-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4eafc-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4eafc-133">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4eafc-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4eafc-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4eafc-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


