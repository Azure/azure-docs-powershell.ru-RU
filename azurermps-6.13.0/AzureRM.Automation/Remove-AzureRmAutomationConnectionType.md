---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 9598280ecae0ce8aca94fd16ae40928dba7a2404
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561199"
---
# <span data-ttu-id="6d8b6-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="6d8b6-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="6d8b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8b6-103">Удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d8b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d8b6-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d8b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d8b6-105">DESCRIPTION</span></span>
<span data-ttu-id="6d8b6-106">Командлет **Remove-AzureRmAutomationConnectionType** удаляет тип подключения из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="6d8b6-107">Все подключения, связанные с удаленным типом соединения, будут недоступны для использования.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="6d8b6-108">Удалите их, если не создать новый тип соединения, отвечающий указанным ниже условиям.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="6d8b6-109">Тип имеет то же имя, что и исходный тип соединения.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="6d8b6-110">Этот тип имеет те же определения полей, что и исходный тип соединения.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="6d8b6-111">У него могут быть дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-111">It can have additional fields.</span></span>

## <span data-ttu-id="6d8b6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d8b6-112">EXAMPLES</span></span>

### <span data-ttu-id="6d8b6-113">Пример 1: Удаление типа подключения</span><span class="sxs-lookup"><span data-stu-id="6d8b6-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6d8b6-114">Эта команда удаляет тип подключения с именем ContosoConnectionType в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6d8b6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d8b6-115">PARAMETERS</span></span>

### <span data-ttu-id="6d8b6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6d8b6-116">-AutomationAccountName</span></span>
<span data-ttu-id="6d8b6-117">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет тип подключения.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="6d8b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8b6-118">-DefaultProfile</span></span>
<span data-ttu-id="6d8b6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6d8b6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d8b6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6d8b6-120">-Force</span></span>
<span data-ttu-id="6d8b6-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="6d8b6-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8b6-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d8b6-122">-Name</span></span>
<span data-ttu-id="6d8b6-123">Указывает имя типа подключения автоматизации, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d8b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d8b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d8b6-125">Указывает имя группы ресурсов, из которой этот командлет удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="6d8b6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d8b6-126">-Confirm</span></span>
<span data-ttu-id="6d8b6-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8b6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d8b6-128">-WhatIf</span></span>
<span data-ttu-id="6d8b6-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d8b6-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d8b6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8b6-131">CommonParameters</span></span>
<span data-ttu-id="6d8b6-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d8b6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8b6-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8b6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8b6-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d8b6-134">INPUTS</span></span>

### <span data-ttu-id="6d8b6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6d8b6-135">System.String</span></span>

## <span data-ttu-id="6d8b6-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d8b6-136">OUTPUTS</span></span>

### <span data-ttu-id="6d8b6-137">System. void</span><span class="sxs-lookup"><span data-stu-id="6d8b6-137">System.Void</span></span>

## <span data-ttu-id="6d8b6-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d8b6-138">NOTES</span></span>

## <span data-ttu-id="6d8b6-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d8b6-139">RELATED LINKS</span></span>

[<span data-ttu-id="6d8b6-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6d8b6-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


