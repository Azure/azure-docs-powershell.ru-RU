---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 6bbdfa981ac1d9e80c377bf2835cff73c99a7a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567132"
---
# <span data-ttu-id="40f88-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="40f88-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="40f88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40f88-102">SYNOPSIS</span></span>
<span data-ttu-id="40f88-103">Удаляет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40f88-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40f88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40f88-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40f88-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40f88-105">DESCRIPTION</span></span>
<span data-ttu-id="40f88-106">Командлет **Remove-AzureRmDataLakeStoreFirewallRule** удаляет указанное правило брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="40f88-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="40f88-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40f88-107">EXAMPLES</span></span>

### <span data-ttu-id="40f88-108">Пример 1: Удаление правила брандмауэра из учетной записи</span><span class="sxs-lookup"><span data-stu-id="40f88-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="40f88-109">Удаление правила брандмауэра "MyFirewallRule" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="40f88-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="40f88-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40f88-110">PARAMETERS</span></span>

### <span data-ttu-id="40f88-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="40f88-111">-Account</span></span>
<span data-ttu-id="40f88-112">Учетная запись Data Lake Store для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="40f88-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="40f88-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40f88-113">-Name</span></span>
<span data-ttu-id="40f88-114">Имя удаляемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="40f88-114">The name of the firewall rule to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f88-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40f88-115">-PassThru</span></span>
<span data-ttu-id="40f88-116">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="40f88-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f88-117">-ResourceGroupName</span></span>
<span data-ttu-id="40f88-118">Указывает имя группы ресурсов, которая содержит учетную запись, из которой нужно удалить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="40f88-118">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="40f88-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40f88-119">-Confirm</span></span>
<span data-ttu-id="40f88-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40f88-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f88-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f88-121">-WhatIf</span></span>
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

### <span data-ttu-id="40f88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f88-122">-DefaultProfile</span></span>
<span data-ttu-id="40f88-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40f88-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40f88-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f88-124">CommonParameters</span></span>
<span data-ttu-id="40f88-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40f88-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f88-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f88-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f88-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40f88-127">INPUTS</span></span>

## <span data-ttu-id="40f88-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40f88-128">OUTPUTS</span></span>

### <span data-ttu-id="40f88-129">логических</span><span class="sxs-lookup"><span data-stu-id="40f88-129">bool</span></span>
<span data-ttu-id="40f88-130">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="40f88-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="40f88-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="40f88-131">NOTES</span></span>

## <span data-ttu-id="40f88-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40f88-132">RELATED LINKS</span></span>

