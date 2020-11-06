---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: c1e4c3f748df4808fe570e95150450d3b3987d00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568595"
---
# <span data-ttu-id="3da91-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3da91-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="3da91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3da91-102">SYNOPSIS</span></span>
<span data-ttu-id="3da91-103">Добавляет правило брандмауэра в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3da91-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3da91-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3da91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3da91-105">DESCRIPTION</span></span>
<span data-ttu-id="3da91-106">Командлет **Add-AzureRmDataLakeStoreFirewallRule** добавляет правило межсетевого экрана для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3da91-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="3da91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3da91-107">EXAMPLES</span></span>

### <span data-ttu-id="3da91-108">Пример 1: Добавление нового правила межсетевого экрана для учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3da91-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="3da91-109">В результате создается новое правило брандмауэра с именем "MyRule" в учетной записи "ContosoADL" с IP-диапазоном 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="3da91-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="3da91-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3da91-110">PARAMETERS</span></span>

### <span data-ttu-id="3da91-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="3da91-111">-Account</span></span>
<span data-ttu-id="3da91-112">Учетная запись Data Lake Store, в которую нужно добавить правило межсетевого экрана</span><span class="sxs-lookup"><span data-stu-id="3da91-112">The Data Lake Store account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da91-113">-DefaultProfile</span></span>
<span data-ttu-id="3da91-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3da91-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3da91-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3da91-115">-EndIpAddress</span></span>
<span data-ttu-id="3da91-116">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="3da91-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da91-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3da91-117">-Name</span></span>
<span data-ttu-id="3da91-118">Имя добавляемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3da91-118">The name of the firewall rule to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da91-119">-ResourceGroupName</span></span>
<span data-ttu-id="3da91-120">Имя группы ресурсов, под которой учетная запись добавляет правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3da91-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da91-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3da91-121">-StartIpAddress</span></span>
<span data-ttu-id="3da91-122">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="3da91-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da91-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3da91-123">-Confirm</span></span>
<span data-ttu-id="3da91-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3da91-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3da91-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3da91-125">-WhatIf</span></span>
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

### <span data-ttu-id="3da91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da91-126">CommonParameters</span></span>
<span data-ttu-id="3da91-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3da91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da91-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da91-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3da91-129">INPUTS</span></span>

### <span data-ttu-id="3da91-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3da91-130">None</span></span>
<span data-ttu-id="3da91-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3da91-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3da91-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3da91-132">OUTPUTS</span></span>

### <span data-ttu-id="3da91-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3da91-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="3da91-134">Добавленное правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3da91-134">The firewall rule that was added.</span></span>

## <span data-ttu-id="3da91-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3da91-135">NOTES</span></span>

## <span data-ttu-id="3da91-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3da91-136">RELATED LINKS</span></span>

