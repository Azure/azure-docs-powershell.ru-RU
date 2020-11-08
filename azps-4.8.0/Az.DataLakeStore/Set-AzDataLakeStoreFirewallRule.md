---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077841"
---
# <span data-ttu-id="16f0f-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16f0f-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="16f0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="16f0f-103">Изменяет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16f0f-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="16f0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16f0f-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16f0f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="16f0f-106">Командлет **Set-AzDataLakeStoreFirewallRule** изменяет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16f0f-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="16f0f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="16f0f-108">Пример 1: изменение начального и конечного IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="16f0f-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="16f0f-109">Обновляет правило брандмауэра "MyFirewallRule" в учетной записи "ContosoADL", чтобы получить диапазон от 127.0.0.1 до 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="16f0f-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="16f0f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16f0f-110">PARAMETERS</span></span>

### <span data-ttu-id="16f0f-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="16f0f-111">-Account</span></span>
<span data-ttu-id="16f0f-112">Учетная запись Data Lake Store для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="16f0f-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="16f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="16f0f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16f0f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16f0f-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="16f0f-115">-EndIpAddress</span></span>
<span data-ttu-id="16f0f-116">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="16f0f-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="16f0f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16f0f-117">-Name</span></span>
<span data-ttu-id="16f0f-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="16f0f-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="16f0f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f0f-119">-ResourceGroupName</span></span>
<span data-ttu-id="16f0f-120">Указывает имя группы ресурсов, которая содержит учетную запись, для которой нужно обновить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="16f0f-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="16f0f-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="16f0f-121">-StartIpAddress</span></span>
<span data-ttu-id="16f0f-122">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="16f0f-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="16f0f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16f0f-123">-Confirm</span></span>
<span data-ttu-id="16f0f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16f0f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f0f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f0f-125">-WhatIf</span></span>
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

### <span data-ttu-id="16f0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f0f-126">CommonParameters</span></span>
<span data-ttu-id="16f0f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16f0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f0f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f0f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f0f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16f0f-129">INPUTS</span></span>

### <span data-ttu-id="16f0f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="16f0f-130">System.String</span></span>

## <span data-ttu-id="16f0f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16f0f-131">OUTPUTS</span></span>

### <span data-ttu-id="16f0f-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="16f0f-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="16f0f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="16f0f-133">NOTES</span></span>

## <span data-ttu-id="16f0f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16f0f-134">RELATED LINKS</span></span>
