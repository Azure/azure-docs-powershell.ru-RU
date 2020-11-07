---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 533013be3a878e946b9ff5e44826ad5a7bd6415d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734022"
---
# <span data-ttu-id="f9ec0-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="f9ec0-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="f9ec0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ec0-103">Обновление учетной записи интеграции, полученной в качестве номера элемента управления ICN, в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9ec0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9ec0-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ec0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ec0-106">Командлет Set-AzureRmIntegrationAccountGeneratedIcn обновляет существующую учетную запись интеграции, полученную с помощью номера управления обменом (ICN), и возвращает объект, представляющий учетную запись интеграции, полученную с помощью номера элемента управления Interchange.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="f9ec0-107">Используйте этот командлет для обновления учетной записи интеграции, которая получила состояние обработки сообщения для номера элемента управления "Обмен".</span><span class="sxs-lookup"><span data-stu-id="f9ec0-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="f9ec0-108">Вы можете обновить учетную запись интеграции, полученную с помощью номера элемента управления обменом, указав имя учетной записи интеграции, имя группы ресурсов, имя соглашения, значение управляющего номера и состояние обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="f9ec0-109">С помощью этой команды вы не можете создать новую учетную запись интеграции с номером элемента управления обменом.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="f9ec0-110">Чтобы использовать динамические параметры, просто введите их в команду или введите знак дефис (-), чтобы указать имя параметра, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f9ec0-111">Если вы пропустили требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="f9ec0-112">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="f9ec0-113">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="f9ec0-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="f9ec0-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9ec0-114">EXAMPLES</span></span>

### <span data-ttu-id="f9ec0-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9ec0-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="f9ec0-116">Эта команда обновляет учетную запись интеграции, полученную X12, для определенного соглашения учетной записи интеграции и значения с состоянием обработки сообщения Failed.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="f9ec0-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f9ec0-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="f9ec0-118">Эта команда обновляет учетную запись интеграции, полученную EDIFACT, для определенного соглашения учетной записи интеграции и значения с состоянием обработки сообщения Failed.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="f9ec0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9ec0-119">PARAMETERS</span></span>

### <span data-ttu-id="f9ec0-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f9ec0-120">-AgreementName</span></span>
<span data-ttu-id="f9ec0-121">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-121">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f9ec0-122">-AgreementType</span></span>
<span data-ttu-id="f9ec0-123">Тип соглашения для учетной записи интеграции (X12 или EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="f9ec0-123">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="f9ec0-124">-ControlNumberValue</span></span>
<span data-ttu-id="f9ec0-125">Значение номера контроля учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-125">The integration account control number value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ec0-126">-DefaultProfile</span></span>
<span data-ttu-id="f9ec0-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f9ec0-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9ec0-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="f9ec0-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="f9ec0-129">Состояние обработки получаемых сообщений.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-129">The received message processing status.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9ec0-130">-Name</span></span>
<span data-ttu-id="f9ec0-131">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-131">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9ec0-132">-ResourceGroupName</span></span>
<span data-ttu-id="f9ec0-133">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="f9ec0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9ec0-134">-Confirm</span></span>
<span data-ttu-id="f9ec0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ec0-136">-WhatIf</span></span>
<span data-ttu-id="f9ec0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9ec0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ec0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ec0-139">CommonParameters</span></span>
<span data-ttu-id="f9ec0-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9ec0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ec0-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ec0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ec0-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9ec0-142">INPUTS</span></span>

### <span data-ttu-id="f9ec0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f9ec0-143">System.String</span></span>

## <span data-ttu-id="f9ec0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9ec0-144">OUTPUTS</span></span>

### <span data-ttu-id="f9ec0-145">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="f9ec0-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="f9ec0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9ec0-146">NOTES</span></span>

## <span data-ttu-id="f9ec0-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9ec0-147">RELATED LINKS</span></span>

<span data-ttu-id="f9ec0-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="f9ec0-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
