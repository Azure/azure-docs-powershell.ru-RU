---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214969"
---
# <span data-ttu-id="e1a80-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e1a80-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e1a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1a80-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a80-103">Изменяет указанное правило брандмауэра в указанном хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="e1a80-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e1a80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1a80-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1a80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1a80-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a80-106">**Cmdlet Set-AzDataLakeStoreFirewallRule** изменяет указанное правило брандмауэра в указанном хранилище data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e1a80-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e1a80-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1a80-107">EXAMPLES</span></span>

### <span data-ttu-id="e1a80-108">Пример 1. Обновление диапазона IP-адресов начала и окончания для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="e1a80-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="e1a80-109">Обновляет правило брандмауэра MyFirewallRule в учетной записи ContosoADL с диапазоном от 127.0.0.1 до 127.0.0.2.</span><span class="sxs-lookup"><span data-stu-id="e1a80-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="e1a80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1a80-110">PARAMETERS</span></span>

### <span data-ttu-id="e1a80-111">-Account</span><span class="sxs-lookup"><span data-stu-id="e1a80-111">-Account</span></span>
<span data-ttu-id="e1a80-112">Учетная запись магазина данных Для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="e1a80-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="e1a80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a80-113">-DefaultProfile</span></span>
<span data-ttu-id="e1a80-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e1a80-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1a80-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1a80-115">-EndIpAddress</span></span>
<span data-ttu-id="e1a80-116">Конец допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="e1a80-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a80-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e1a80-117">-Name</span></span>
<span data-ttu-id="e1a80-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e1a80-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="e1a80-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a80-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1a80-120">Имя группы ресурсов, содержачей учетную запись, для которую нужно обновить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e1a80-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a80-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e1a80-121">-StartIpAddress</span></span>
<span data-ttu-id="e1a80-122">Начало допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="e1a80-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a80-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1a80-123">-Confirm</span></span>
<span data-ttu-id="e1a80-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1a80-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1a80-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1a80-125">-WhatIf</span></span>
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

### <span data-ttu-id="e1a80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a80-126">CommonParameters</span></span>
<span data-ttu-id="e1a80-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a80-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a80-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a80-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1a80-129">INPUTS</span></span>

### <span data-ttu-id="e1a80-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e1a80-130">System.String</span></span>

## <span data-ttu-id="e1a80-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1a80-131">OUTPUTS</span></span>

### <span data-ttu-id="e1a80-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e1a80-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e1a80-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1a80-133">NOTES</span></span>

## <span data-ttu-id="e1a80-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1a80-134">RELATED LINKS</span></span>
