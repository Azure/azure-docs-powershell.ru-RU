---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228772"
---
# <span data-ttu-id="7d1db-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7d1db-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="7d1db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1db-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1db-103">Добавляет правило брандмауэра к указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d1db-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="7d1db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d1db-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d1db-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1db-106">Для указанной учетной записи Data Lake Store будет добавлено правило брандмауэра **Add-AzDataLakeStoreFirewallRule.**</span><span class="sxs-lookup"><span data-stu-id="7d1db-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="7d1db-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d1db-107">EXAMPLES</span></span>

### <span data-ttu-id="7d1db-108">Пример 1. Добавление нового правила брандмауэра в учетную запись Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7d1db-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="7d1db-109">При этом создается новое правило брандмауэра под названием "MyRule" в учетной записи ContosoADL с диапазоном IP-адресов 127.0.0.1–127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="7d1db-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="7d1db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d1db-110">PARAMETERS</span></span>

### <span data-ttu-id="7d1db-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7d1db-111">-Account</span></span>
<span data-ttu-id="7d1db-112">Учетная запись Магазина данных для добавления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="7d1db-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="7d1db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1db-113">-DefaultProfile</span></span>
<span data-ttu-id="7d1db-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d1db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d1db-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d1db-115">-EndIpAddress</span></span>
<span data-ttu-id="7d1db-116">Конец допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7d1db-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="7d1db-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7d1db-117">-Name</span></span>
<span data-ttu-id="7d1db-118">Имя добавляемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7d1db-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="7d1db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1db-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d1db-120">Имя группы ресурсов, для которой нужно добавить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7d1db-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="7d1db-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d1db-121">-StartIpAddress</span></span>
<span data-ttu-id="7d1db-122">Начало допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7d1db-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="7d1db-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d1db-123">-Confirm</span></span>
<span data-ttu-id="7d1db-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d1db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1db-125">-WhatIf</span></span>
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

### <span data-ttu-id="7d1db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1db-126">CommonParameters</span></span>
<span data-ttu-id="7d1db-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1db-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1db-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1db-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d1db-129">INPUTS</span></span>

### <span data-ttu-id="7d1db-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7d1db-130">System.String</span></span>

## <span data-ttu-id="7d1db-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d1db-131">OUTPUTS</span></span>

### <span data-ttu-id="7d1db-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7d1db-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="7d1db-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d1db-133">NOTES</span></span>

## <span data-ttu-id="7d1db-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d1db-134">RELATED LINKS</span></span>
