---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: cc85bea2739c379e960ffee29250bdc172e36765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563956"
---
# <span data-ttu-id="75b3b-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="75b3b-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="75b3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="75b3b-103">Получает или перечисляет DNS-псевдоним Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75b3b-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75b3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75b3b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="75b3b-106">Получите конкретный DNS-псевдоним для Azure SQL Server или список всех DNS-псевдонимов сервера.</span><span class="sxs-lookup"><span data-stu-id="75b3b-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="75b3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75b3b-107">EXAMPLES</span></span>

### <span data-ttu-id="75b3b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75b3b-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="75b3b-109">Вывод списка всех DNS-псевдонимов сервера для определенного сервера</span><span class="sxs-lookup"><span data-stu-id="75b3b-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="75b3b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75b3b-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="75b3b-111">Получает псевдоним DNS сервера, указанный именем сервера и псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="75b3b-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="75b3b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75b3b-112">PARAMETERS</span></span>

### <span data-ttu-id="75b3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b3b-113">-DefaultProfile</span></span>
<span data-ttu-id="75b3b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75b3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75b3b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75b3b-115">-Name</span></span>
<span data-ttu-id="75b3b-116">Имя псевдонима DNS для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75b3b-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b3b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b3b-117">-ResourceGroupName</span></span>
<span data-ttu-id="75b3b-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75b3b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="75b3b-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="75b3b-119">-ServerName</span></span>
<span data-ttu-id="75b3b-120">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75b3b-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="75b3b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75b3b-121">-Confirm</span></span>
<span data-ttu-id="75b3b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75b3b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b3b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b3b-123">-WhatIf</span></span>
<span data-ttu-id="75b3b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75b3b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b3b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75b3b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b3b-126">CommonParameters</span></span>
<span data-ttu-id="75b3b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75b3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b3b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b3b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b3b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75b3b-129">INPUTS</span></span>

### <span data-ttu-id="75b3b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75b3b-130">System.String</span></span>

## <span data-ttu-id="75b3b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75b3b-131">OUTPUTS</span></span>

### <span data-ttu-id="75b3b-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="75b3b-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="75b3b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="75b3b-133">NOTES</span></span>

## <span data-ttu-id="75b3b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75b3b-134">RELATED LINKS</span></span>
