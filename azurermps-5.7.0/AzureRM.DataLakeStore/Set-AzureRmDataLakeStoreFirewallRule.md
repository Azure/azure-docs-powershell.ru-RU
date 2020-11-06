---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566191"
---
# <span data-ttu-id="c9724-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9724-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="c9724-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9724-102">SYNOPSIS</span></span>
<span data-ttu-id="c9724-103">Изменяет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9724-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9724-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9724-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9724-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9724-105">DESCRIPTION</span></span>
<span data-ttu-id="c9724-106">Командлет **Set-AzureRmDataLakeStoreFirewallRule** изменяет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c9724-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="c9724-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9724-107">EXAMPLES</span></span>

### <span data-ttu-id="c9724-108">Пример 1: изменение начального и конечного IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c9724-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="c9724-109">Обновляет правило брандмауэра "MyFirewallRule" в учетной записи "ContosoADL", чтобы получить диапазон от 127.0.0.1 до 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="c9724-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="c9724-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9724-110">PARAMETERS</span></span>

### <span data-ttu-id="c9724-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c9724-111">-Account</span></span>
<span data-ttu-id="c9724-112">Учетная запись Data Lake Store для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="c9724-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="c9724-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9724-113">-DefaultProfile</span></span>
<span data-ttu-id="c9724-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c9724-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9724-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c9724-115">-EndIpAddress</span></span>
<span data-ttu-id="c9724-116">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c9724-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9724-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9724-117">-Name</span></span>
<span data-ttu-id="c9724-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c9724-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="c9724-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9724-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9724-120">Указывает имя группы ресурсов, которая содержит учетную запись, для которой нужно обновить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c9724-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9724-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c9724-121">-StartIpAddress</span></span>
<span data-ttu-id="c9724-122">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c9724-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9724-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9724-123">-Confirm</span></span>
<span data-ttu-id="c9724-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9724-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9724-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9724-125">-WhatIf</span></span>
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

### <span data-ttu-id="c9724-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9724-126">CommonParameters</span></span>
<span data-ttu-id="c9724-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9724-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9724-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9724-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9724-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9724-129">INPUTS</span></span>

### <span data-ttu-id="c9724-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="c9724-130">None</span></span>
<span data-ttu-id="c9724-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c9724-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9724-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9724-132">OUTPUTS</span></span>

### <span data-ttu-id="c9724-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c9724-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="c9724-134">Подробное описание обновленного правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c9724-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="c9724-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9724-135">NOTES</span></span>

## <span data-ttu-id="c9724-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9724-136">RELATED LINKS</span></span>

