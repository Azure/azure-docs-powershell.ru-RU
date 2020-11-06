---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: be42bd7d3e4a6a839182ae36d71f73377460eceb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559727"
---
# <span data-ttu-id="c3582-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c3582-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="c3582-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3582-102">SYNOPSIS</span></span>
<span data-ttu-id="c3582-103">Этот командлет извлекает конкретный номер полученного элемента управления обменом для каждого соглашения и значения Control Number.</span><span class="sxs-lookup"><span data-stu-id="c3582-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3582-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3582-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3582-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3582-105">DESCRIPTION</span></span>
<span data-ttu-id="c3582-106">Этот командлет предназначен для использования в сценариях аварийного восстановления для проверки наличия полученного номера управления обменом и, при необходимости, для удаления этого объекта с помощью Remove-AzureRmIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="c3582-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="c3582-107">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="c3582-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c3582-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3582-108">EXAMPLES</span></span>

### <span data-ttu-id="c3582-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3582-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="c3582-110">Эта команда получает учетную запись интеграции X12, которая получила номер управляющего элемента управления обменом по названию соглашения и значению контрольного номера.</span><span class="sxs-lookup"><span data-stu-id="c3582-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="c3582-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c3582-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="c3582-112">Эта команда получает учетную запись интеграции EDIFACT, которая получила номер управляющего элемента управления обменом по названию соглашения и значению контрольного номера.</span><span class="sxs-lookup"><span data-stu-id="c3582-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="c3582-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3582-113">PARAMETERS</span></span>

### <span data-ttu-id="c3582-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c3582-114">-AgreementName</span></span>
<span data-ttu-id="c3582-115">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3582-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="c3582-116">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="c3582-116">-ControlNumberValue</span></span>
<span data-ttu-id="c3582-117">Значение номера контроля учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3582-117">The integration account control number value.</span></span>

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

### <span data-ttu-id="c3582-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3582-118">-Name</span></span>
<span data-ttu-id="c3582-119">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3582-119">The integration account name.</span></span>

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

### <span data-ttu-id="c3582-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3582-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3582-121">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3582-121">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c3582-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="c3582-122">-AgreementType</span></span>
<span data-ttu-id="c3582-123">Тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c3582-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3582-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3582-124">-DefaultProfile</span></span>
<span data-ttu-id="c3582-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3582-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3582-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3582-126">CommonParameters</span></span>
<span data-ttu-id="c3582-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3582-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3582-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3582-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3582-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3582-129">INPUTS</span></span>

### <span data-ttu-id="c3582-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c3582-130">System.String</span></span>

## <span data-ttu-id="c3582-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3582-131">OUTPUTS</span></span>

### <span data-ttu-id="c3582-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountClient + IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="c3582-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="c3582-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3582-133">NOTES</span></span>

## <span data-ttu-id="c3582-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3582-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3582-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c3582-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="c3582-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="c3582-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
