---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235609"
---
# <span data-ttu-id="b6006-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6006-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b6006-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6006-102">SYNOPSIS</span></span>
<span data-ttu-id="b6006-103">Добавляет правило брандмауэра в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6006-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b6006-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6006-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6006-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6006-105">DESCRIPTION</span></span>
<span data-ttu-id="b6006-106">Командлет **Add-AzDataLakeStoreFirewallRule** добавляет правило межсетевого экрана для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6006-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b6006-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6006-107">EXAMPLES</span></span>

### <span data-ttu-id="b6006-108">Пример 1: Добавление нового правила межсетевого экрана для учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b6006-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="b6006-109">В результате создается новое правило брандмауэра с именем "MyRule" в учетной записи "ContosoADL" с IP-диапазоном 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="b6006-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="b6006-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6006-110">PARAMETERS</span></span>

### <span data-ttu-id="b6006-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b6006-111">-Account</span></span>
<span data-ttu-id="b6006-112">Учетная запись Data Lake Store, в которую нужно добавить правило межсетевого экрана</span><span class="sxs-lookup"><span data-stu-id="b6006-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6006-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6006-113">-DefaultProfile</span></span>
<span data-ttu-id="b6006-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6006-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6006-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6006-115">-EndIpAddress</span></span>
<span data-ttu-id="b6006-116">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b6006-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6006-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6006-117">-Name</span></span>
<span data-ttu-id="b6006-118">Имя добавляемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b6006-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="b6006-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6006-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6006-120">Имя группы ресурсов, под которой учетная запись добавляет правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="b6006-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6006-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6006-121">-StartIpAddress</span></span>
<span data-ttu-id="b6006-122">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="b6006-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="b6006-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6006-123">-Confirm</span></span>
<span data-ttu-id="b6006-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6006-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6006-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6006-125">-WhatIf</span></span>
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

### <span data-ttu-id="b6006-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6006-126">CommonParameters</span></span>
<span data-ttu-id="b6006-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6006-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6006-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6006-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6006-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6006-129">INPUTS</span></span>

### <span data-ttu-id="b6006-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b6006-130">System.String</span></span>

## <span data-ttu-id="b6006-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6006-131">OUTPUTS</span></span>

### <span data-ttu-id="b6006-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6006-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b6006-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6006-133">NOTES</span></span>

## <span data-ttu-id="b6006-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6006-134">RELATED LINKS</span></span>
