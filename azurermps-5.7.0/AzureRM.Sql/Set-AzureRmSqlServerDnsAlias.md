---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 78ffcb50b47b315426998825232348dd41c23f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558783"
---
# <span data-ttu-id="71d9d-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="71d9d-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="71d9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="71d9d-103">Изменяет сервер, на который указывает DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="71d9d-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71d9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71d9d-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="71d9d-106">Эта команда обновляет сервер, на который указывает псевдоним.</span><span class="sxs-lookup"><span data-stu-id="71d9d-106">This command is updating the server to which alias is pointing.</span></span> 

<span data-ttu-id="71d9d-107">Эта команда должна быть выполнена при входе в подписку, в которой находится новый сервер, на который будет указывать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="71d9d-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="71d9d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71d9d-108">EXAMPLES</span></span>

### <span data-ttu-id="71d9d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71d9d-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="71d9d-110">Эта команда обновляет псевдоним, который ранее указывал на oldServer для указания на сервер newServer</span><span class="sxs-lookup"><span data-stu-id="71d9d-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="71d9d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71d9d-111">PARAMETERS</span></span>

### <span data-ttu-id="71d9d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71d9d-112">-AsJob</span></span>
<span data-ttu-id="71d9d-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="71d9d-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="71d9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d9d-114">-DefaultProfile</span></span>
<span data-ttu-id="71d9d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71d9d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71d9d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71d9d-116">-Name</span></span>
<span data-ttu-id="71d9d-117">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="71d9d-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d9d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d9d-118">-ResourceGroupName</span></span>
<span data-ttu-id="71d9d-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71d9d-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d9d-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="71d9d-120">-SourceServerName</span></span>
<span data-ttu-id="71d9d-121">Имя сервера Azure SQL Server, на который в данный момент указывает псевдоним.</span><span class="sxs-lookup"><span data-stu-id="71d9d-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9d-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d9d-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="71d9d-123">Имя группы ресурсов исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="71d9d-123">The name of resource group of the source server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9d-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71d9d-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="71d9d-125">Идентификатор подписки исходного сервера</span><span class="sxs-lookup"><span data-stu-id="71d9d-125">The subscription id of the source server</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9d-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="71d9d-126">-TargetServerName</span></span>
<span data-ttu-id="71d9d-127">Имя сервера Azure SQL Server, на который должна указывать псевдоним.</span><span class="sxs-lookup"><span data-stu-id="71d9d-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d9d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71d9d-128">-Confirm</span></span>
<span data-ttu-id="71d9d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71d9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d9d-130">-WhatIf</span></span>
<span data-ttu-id="71d9d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71d9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71d9d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71d9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d9d-133">CommonParameters</span></span>
<span data-ttu-id="71d9d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71d9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d9d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d9d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d9d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71d9d-136">INPUTS</span></span>

### <span data-ttu-id="71d9d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="71d9d-137">System.String</span></span>

## <span data-ttu-id="71d9d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d9d-138">OUTPUTS</span></span>

### <span data-ttu-id="71d9d-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="71d9d-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="71d9d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="71d9d-140">NOTES</span></span>

## <span data-ttu-id="71d9d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71d9d-141">RELATED LINKS</span></span>
