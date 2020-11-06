---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 6c18639e3c717ced8ed107ce3604e20639d87682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562556"
---
# <span data-ttu-id="cbe1b-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="cbe1b-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="cbe1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbe1b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe1b-103">Изменяет сервер, на который указывает DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbe1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbe1b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbe1b-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe1b-106">Эта команда обновляет сервер, на который указывает псевдоним.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="cbe1b-107">Эта команда должна быть выполнена при входе в подписку, в которой находится новый сервер, на который будет указывать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="cbe1b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbe1b-108">EXAMPLES</span></span>

### <span data-ttu-id="cbe1b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cbe1b-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="cbe1b-110">Эта команда обновляет псевдоним, который ранее указывал на oldServer для указания на сервер newServer</span><span class="sxs-lookup"><span data-stu-id="cbe1b-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="cbe1b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbe1b-111">PARAMETERS</span></span>

### <span data-ttu-id="cbe1b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbe1b-112">-AsJob</span></span>
<span data-ttu-id="cbe1b-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cbe1b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbe1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe1b-114">-DefaultProfile</span></span>
<span data-ttu-id="cbe1b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbe1b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbe1b-116">-Name</span></span>
<span data-ttu-id="cbe1b-117">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbe1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="cbe1b-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbe1b-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="cbe1b-120">-SourceServerName</span></span>
<span data-ttu-id="cbe1b-121">Имя сервера Azure SQL Server, на который в данный момент указывает псевдоним.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="cbe1b-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe1b-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="cbe1b-123">Имя группы ресурсов исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="cbe1b-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbe1b-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="cbe1b-125">Идентификатор подписки исходного сервера</span><span class="sxs-lookup"><span data-stu-id="cbe1b-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe1b-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="cbe1b-126">-TargetServerName</span></span>
<span data-ttu-id="cbe1b-127">Имя сервера Azure SQL Server, на который должна указывать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="cbe1b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbe1b-128">-Confirm</span></span>
<span data-ttu-id="cbe1b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe1b-130">-WhatIf</span></span>
<span data-ttu-id="cbe1b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbe1b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe1b-133">CommonParameters</span></span>
<span data-ttu-id="cbe1b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbe1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe1b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe1b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbe1b-136">INPUTS</span></span>

### <span data-ttu-id="cbe1b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cbe1b-137">System.String</span></span>

## <span data-ttu-id="cbe1b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbe1b-138">OUTPUTS</span></span>

### <span data-ttu-id="cbe1b-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="cbe1b-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="cbe1b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbe1b-140">NOTES</span></span>

## <span data-ttu-id="cbe1b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbe1b-141">RELATED LINKS</span></span>
