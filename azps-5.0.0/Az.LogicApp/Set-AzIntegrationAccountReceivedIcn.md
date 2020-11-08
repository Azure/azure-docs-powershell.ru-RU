---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247707"
---
# <span data-ttu-id="ec4e3-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="ec4e3-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="ec4e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4e3-103">Обновление учетной записи интеграции, полученной в качестве номера элемента управления ICN, в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="ec4e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec4e3-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec4e3-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4e3-106">Командлет Set-AzIntegrationAccountGeneratedIcn обновляет существующую учетную запись интеграции, полученную с помощью номера управления обменом (ICN), и возвращает объект, представляющий учетную запись интеграции, полученную с помощью номера элемента управления Interchange.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="ec4e3-107">Используйте этот командлет для обновления учетной записи интеграции, которая получила состояние обработки сообщения для номера элемента управления "Обмен".</span><span class="sxs-lookup"><span data-stu-id="ec4e3-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="ec4e3-108">Вы можете обновить учетную запись интеграции, полученную с помощью номера элемента управления обменом, указав имя учетной записи интеграции, имя группы ресурсов, имя соглашения, значение управляющего номера и состояние обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="ec4e3-109">С помощью этой команды вы не можете создать новую учетную запись интеграции с номером элемента управления обменом.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="ec4e3-110">Чтобы использовать динамические параметры, просто введите их в команду или введите знак дефис (-), чтобы указать имя параметра, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ec4e3-111">Если вы пропустили требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="ec4e3-112">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ec4e3-113">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="ec4e3-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="ec4e3-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec4e3-114">EXAMPLES</span></span>

### <span data-ttu-id="ec4e3-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec4e3-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="ec4e3-116">Эта команда обновляет учетную запись интеграции, полученную X12, для определенного соглашения учетной записи интеграции и значения с состоянием обработки сообщения Failed.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="ec4e3-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ec4e3-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="ec4e3-118">Эта команда обновляет учетную запись интеграции, полученную EDIFACT, для определенного соглашения учетной записи интеграции и значения с состоянием обработки сообщения Failed.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="ec4e3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec4e3-119">PARAMETERS</span></span>

### <span data-ttu-id="ec4e3-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="ec4e3-120">-AgreementName</span></span>
<span data-ttu-id="ec4e3-121">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-121">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e3-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="ec4e3-122">-AgreementType</span></span>
<span data-ttu-id="ec4e3-123">Тип соглашения для учетной записи интеграции (X12 или EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="ec4e3-123">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e3-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="ec4e3-124">-ControlNumberValue</span></span>
<span data-ttu-id="ec4e3-125">Значение номера контроля учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-125">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4e3-126">-DefaultProfile</span></span>
<span data-ttu-id="ec4e3-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ec4e3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec4e3-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="ec4e3-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="ec4e3-129">Состояние обработки получаемых сообщений.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e3-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec4e3-130">-Name</span></span>
<span data-ttu-id="ec4e3-131">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-131">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4e3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4e3-132">-ResourceGroupName</span></span>
<span data-ttu-id="ec4e3-133">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="ec4e3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec4e3-134">-Confirm</span></span>
<span data-ttu-id="ec4e3-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4e3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4e3-136">-WhatIf</span></span>
<span data-ttu-id="ec4e3-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4e3-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4e3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4e3-139">CommonParameters</span></span>
<span data-ttu-id="ec4e3-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec4e3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4e3-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec4e3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4e3-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec4e3-142">INPUTS</span></span>

### <span data-ttu-id="ec4e3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ec4e3-143">System.String</span></span>

## <span data-ttu-id="ec4e3-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec4e3-144">OUTPUTS</span></span>

### <span data-ttu-id="ec4e3-145">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="ec4e3-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="ec4e3-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec4e3-146">NOTES</span></span>

## <span data-ttu-id="ec4e3-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec4e3-147">RELATED LINKS</span></span>

<span data-ttu-id="ec4e3-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="ec4e3-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
