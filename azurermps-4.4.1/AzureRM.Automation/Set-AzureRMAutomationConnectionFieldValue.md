---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: c3f889f45a90b127287821afb789eab2908faffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568344"
---
# <span data-ttu-id="5a446-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="5a446-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="5a446-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a446-102">SYNOPSIS</span></span>
<span data-ttu-id="5a446-103">Изменяет значение поля в соединении автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5a446-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a446-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a446-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a446-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a446-105">DESCRIPTION</span></span>
<span data-ttu-id="5a446-106">Командлет **Set-AzureRmAutomationConnectionFieldValue** изменяет значение поля в соединении в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="5a446-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="5a446-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a446-107">EXAMPLES</span></span>

### <span data-ttu-id="5a446-108">Пример 1: изменение значения поля в соединении</span><span class="sxs-lookup"><span data-stu-id="5a446-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="5a446-109">Эта команда изменяет идентификатор подписки для подключения Azure с именем ContosoConnection в учетной записи автоматизации с именем AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5a446-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="5a446-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a446-110">PARAMETERS</span></span>

### <span data-ttu-id="5a446-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5a446-111">-AutomationAccountName</span></span>
<span data-ttu-id="5a446-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="5a446-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="5a446-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="5a446-113">-ConnectionFieldName</span></span>
<span data-ttu-id="5a446-114">Задает имя поля, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a446-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a446-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a446-115">-Name</span></span>
<span data-ttu-id="5a446-116">Указывает имя подключения, для которого этот командлет изменяет поле.</span><span class="sxs-lookup"><span data-stu-id="5a446-116">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="5a446-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a446-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a446-118">Указывает имя группы ресурсов, для которой этот командлет изменяет поле в соединении.</span><span class="sxs-lookup"><span data-stu-id="5a446-118">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="5a446-119">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="5a446-119">-Value</span></span>
<span data-ttu-id="5a446-120">Задает значение, которое нужно изменить, в поле Connection (соединение).</span><span class="sxs-lookup"><span data-stu-id="5a446-120">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a446-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a446-121">-DefaultProfile</span></span>
<span data-ttu-id="5a446-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a446-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a446-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a446-123">CommonParameters</span></span>
<span data-ttu-id="5a446-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a446-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a446-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a446-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a446-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a446-126">INPUTS</span></span>

## <span data-ttu-id="5a446-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a446-127">OUTPUTS</span></span>

### <span data-ttu-id="5a446-128">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="5a446-128">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="5a446-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a446-129">NOTES</span></span>

## <span data-ttu-id="5a446-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a446-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a446-131">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="5a446-131">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


