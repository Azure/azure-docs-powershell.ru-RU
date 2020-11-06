---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 5afd12ac027b19f888eb6a5110db2179dd6df24d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568844"
---
# <span data-ttu-id="b726c-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="b726c-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="b726c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b726c-102">SYNOPSIS</span></span>
<span data-ttu-id="b726c-103">Удаляет DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b726c-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b726c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b726c-104">SYNTAX</span></span>

### <span data-ttu-id="b726c-105">Удаление DNS-псевдонима сервера из входных параметров командлета</span><span class="sxs-lookup"><span data-stu-id="b726c-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b726c-106">Удаление псевдонима DNS сервера из определения экземпляра AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b726c-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b726c-107">Удаление DNS-псевдонима сервера из идентификатора ресурса Azure</span><span class="sxs-lookup"><span data-stu-id="b726c-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b726c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b726c-108">DESCRIPTION</span></span>
<span data-ttu-id="b726c-109">Эти команды удаляют псевдоним DNS для Azure SQL Server с сервера, оставив сервер неизменным.</span><span class="sxs-lookup"><span data-stu-id="b726c-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="b726c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b726c-110">EXAMPLES</span></span>

### <span data-ttu-id="b726c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b726c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="b726c-112">Удаляет DNS-псевдоним Azure SQL Server с именем aliasName с сервера с именем serverName.</span><span class="sxs-lookup"><span data-stu-id="b726c-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="b726c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b726c-113">PARAMETERS</span></span>

### <span data-ttu-id="b726c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b726c-114">-AsJob</span></span>
<span data-ttu-id="b726c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b726c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b726c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b726c-116">-DefaultProfile</span></span>
<span data-ttu-id="b726c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b726c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b726c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b726c-118">-Force</span></span>
<span data-ttu-id="b726c-119">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="b726c-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b726c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b726c-120">-InputObject</span></span>
<span data-ttu-id="b726c-121">Удаляемый объект DNS-псевдоним сервера</span><span class="sxs-lookup"><span data-stu-id="b726c-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b726c-122">-Name</span></span>
<span data-ttu-id="b726c-123">Имя псевдонима DNS для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b726c-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b726c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b726c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b726c-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b726c-126">-ResourceId</span></span>
<span data-ttu-id="b726c-127">Идентификатор ресурса удаляемого объекта DNS-псевдонима сервера</span><span class="sxs-lookup"><span data-stu-id="b726c-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b726c-128">-ServerName</span></span>
<span data-ttu-id="b726c-129">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b726c-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b726c-130">-Confirm</span></span>
<span data-ttu-id="b726c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b726c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b726c-132">-WhatIf</span></span>
<span data-ttu-id="b726c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b726c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b726c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b726c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b726c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b726c-135">CommonParameters</span></span>
<span data-ttu-id="b726c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b726c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b726c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b726c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b726c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b726c-138">INPUTS</span></span>

### <span data-ttu-id="b726c-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b726c-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>
<span data-ttu-id="b726c-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b726c-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b726c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b726c-141">System.String</span></span>

## <span data-ttu-id="b726c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b726c-142">OUTPUTS</span></span>

### <span data-ttu-id="b726c-143">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b726c-143">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="b726c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b726c-144">NOTES</span></span>

## <span data-ttu-id="b726c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b726c-145">RELATED LINKS</span></span>
