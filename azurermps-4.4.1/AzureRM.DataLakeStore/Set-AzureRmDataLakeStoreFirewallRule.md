---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733380"
---
# <span data-ttu-id="5b235-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5b235-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="5b235-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b235-102">SYNOPSIS</span></span>
<span data-ttu-id="5b235-103">Изменяет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5b235-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b235-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b235-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b235-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b235-105">DESCRIPTION</span></span>
<span data-ttu-id="5b235-106">Командлет **Set-AzureRmDataLakeStoreFirewallRule** изменяет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5b235-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="5b235-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b235-107">EXAMPLES</span></span>

### <span data-ttu-id="5b235-108">Пример 1: изменение начального и конечного IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5b235-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="5b235-109">Обновляет правило брандмауэра "MyFirewallRule" в учетной записи "ContosoADL", чтобы получить диапазон от 127.0.0.1 до 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="5b235-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="5b235-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b235-110">PARAMETERS</span></span>

### <span data-ttu-id="5b235-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5b235-111">-Account</span></span>
<span data-ttu-id="5b235-112">Учетная запись Data Lake Store для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="5b235-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="5b235-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b235-113">-EndIpAddress</span></span>
<span data-ttu-id="5b235-114">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5b235-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5b235-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b235-115">-Name</span></span>
<span data-ttu-id="5b235-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5b235-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="5b235-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b235-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b235-118">Указывает имя группы ресурсов, которая содержит учетную запись, для которой нужно обновить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5b235-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="5b235-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5b235-119">-StartIpAddress</span></span>
<span data-ttu-id="5b235-120">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5b235-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="5b235-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b235-121">-Confirm</span></span>
<span data-ttu-id="5b235-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b235-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b235-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b235-123">-WhatIf</span></span>
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

### <span data-ttu-id="5b235-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b235-124">-DefaultProfile</span></span>
<span data-ttu-id="5b235-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b235-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b235-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b235-126">CommonParameters</span></span>
<span data-ttu-id="5b235-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b235-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b235-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b235-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b235-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b235-129">INPUTS</span></span>

## <span data-ttu-id="5b235-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b235-130">OUTPUTS</span></span>

### <span data-ttu-id="5b235-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5b235-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="5b235-132">Подробное описание обновленного правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5b235-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="5b235-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b235-133">NOTES</span></span>

## <span data-ttu-id="5b235-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b235-134">RELATED LINKS</span></span>

