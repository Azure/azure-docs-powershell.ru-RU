---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: 84da08588838982353bc8c39354452bec1a17a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567481"
---
# <span data-ttu-id="f328f-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="f328f-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="f328f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f328f-102">SYNOPSIS</span></span>
<span data-ttu-id="f328f-103">Изменяет значение поля в соединении автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f328f-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f328f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f328f-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f328f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f328f-105">DESCRIPTION</span></span>
<span data-ttu-id="f328f-106">Командлет **Set-AzureRmAutomationConnectionFieldValue** изменяет значение поля в соединении в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f328f-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="f328f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f328f-107">EXAMPLES</span></span>

### <span data-ttu-id="f328f-108">Пример 1: изменение значения поля в соединении</span><span class="sxs-lookup"><span data-stu-id="f328f-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="f328f-109">Эта команда изменяет идентификатор подписки для подключения Azure с именем ContosoConnection в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="f328f-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="f328f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f328f-110">PARAMETERS</span></span>

### <span data-ttu-id="f328f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f328f-111">-AutomationAccountName</span></span>
<span data-ttu-id="f328f-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="f328f-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="f328f-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="f328f-113">-ConnectionFieldName</span></span>
<span data-ttu-id="f328f-114">Задает имя поля, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f328f-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f328f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f328f-115">-DefaultProfile</span></span>
<span data-ttu-id="f328f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f328f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f328f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f328f-117">-Name</span></span>
<span data-ttu-id="f328f-118">Указывает имя подключения, для которого этот командлет изменяет поле.</span><span class="sxs-lookup"><span data-stu-id="f328f-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="f328f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f328f-119">-ResourceGroupName</span></span>
<span data-ttu-id="f328f-120">Указывает имя группы ресурсов, для которой этот командлет изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="f328f-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f328f-121">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="f328f-121">-Value</span></span>
<span data-ttu-id="f328f-122">Задает значение, которое нужно изменить, в поле Connection (соединение).</span><span class="sxs-lookup"><span data-stu-id="f328f-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f328f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f328f-123">CommonParameters</span></span>
<span data-ttu-id="f328f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f328f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f328f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f328f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f328f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f328f-126">INPUTS</span></span>

### <span data-ttu-id="f328f-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="f328f-127">None</span></span>
<span data-ttu-id="f328f-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f328f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f328f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f328f-129">OUTPUTS</span></span>

### <span data-ttu-id="f328f-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="f328f-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="f328f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f328f-131">NOTES</span></span>

## <span data-ttu-id="f328f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f328f-132">RELATED LINKS</span></span>

[<span data-ttu-id="f328f-133">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f328f-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


