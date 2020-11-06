---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationConnectionType.md
ms.openlocfilehash: 409a1eca9083c51f501293e4ca37150ce0c328e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565674"
---
# <span data-ttu-id="c0eef-101">Remove-AzureRmAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="c0eef-101">Remove-AzureRmAutomationConnectionType</span></span>

## <span data-ttu-id="c0eef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0eef-102">SYNOPSIS</span></span>
<span data-ttu-id="c0eef-103">Удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c0eef-103">Removes an Automation connection type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0eef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0eef-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0eef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0eef-105">DESCRIPTION</span></span>
<span data-ttu-id="c0eef-106">Командлет **Remove-AzureRmAutomationConnectionType** удаляет тип подключения из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c0eef-106">The **Remove-AzureRmAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>

<span data-ttu-id="c0eef-107">Все подключения, связанные с удаленным типом соединения, будут недоступны для использования.</span><span class="sxs-lookup"><span data-stu-id="c0eef-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="c0eef-108">Удалите их, если не создать новый тип соединения, отвечающий указанным ниже условиям.</span><span class="sxs-lookup"><span data-stu-id="c0eef-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 

- <span data-ttu-id="c0eef-109">Тип имеет то же имя, что и исходный тип соединения.</span><span class="sxs-lookup"><span data-stu-id="c0eef-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="c0eef-110">Этот тип имеет те же определения полей, что и исходный тип соединения.</span><span class="sxs-lookup"><span data-stu-id="c0eef-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="c0eef-111">У него могут быть дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="c0eef-111">It can have additional fields.</span></span>

## <span data-ttu-id="c0eef-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0eef-112">EXAMPLES</span></span>

### <span data-ttu-id="c0eef-113">Пример 1: Удаление типа подключения</span><span class="sxs-lookup"><span data-stu-id="c0eef-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzureRmAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0eef-114">Эта команда удаляет тип подключения с именем ContosoConnectionType в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0eef-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c0eef-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0eef-115">PARAMETERS</span></span>

### <span data-ttu-id="c0eef-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0eef-116">-AutomationAccountName</span></span>
<span data-ttu-id="c0eef-117">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет тип подключения.</span><span class="sxs-lookup"><span data-stu-id="c0eef-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="c0eef-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c0eef-118">-Force</span></span>
<span data-ttu-id="c0eef-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="c0eef-119">ps_force</span></span>

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

### <span data-ttu-id="c0eef-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0eef-120">-Name</span></span>
<span data-ttu-id="c0eef-121">Указывает имя типа подключения автоматизации, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c0eef-121">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0eef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0eef-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0eef-123">Указывает имя группы ресурсов, из которой этот командлет удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c0eef-123">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="c0eef-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0eef-124">-Confirm</span></span>
<span data-ttu-id="c0eef-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0eef-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0eef-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0eef-126">-WhatIf</span></span>
<span data-ttu-id="c0eef-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0eef-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0eef-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0eef-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0eef-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0eef-129">-DefaultProfile</span></span>
<span data-ttu-id="c0eef-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0eef-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0eef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0eef-131">CommonParameters</span></span>
<span data-ttu-id="c0eef-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0eef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0eef-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0eef-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0eef-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0eef-134">INPUTS</span></span>

## <span data-ttu-id="c0eef-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0eef-135">OUTPUTS</span></span>

## <span data-ttu-id="c0eef-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0eef-136">NOTES</span></span>

## <span data-ttu-id="c0eef-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0eef-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0eef-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c0eef-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


