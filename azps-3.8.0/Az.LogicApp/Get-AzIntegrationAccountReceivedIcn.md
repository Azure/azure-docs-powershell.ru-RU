---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912214"
---
# <span data-ttu-id="e4689-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="e4689-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="e4689-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4689-102">SYNOPSIS</span></span>
<span data-ttu-id="e4689-103">Этот командлет извлекает конкретный номер полученного элемента управления обменом для каждого соглашения и значения Control Number.</span><span class="sxs-lookup"><span data-stu-id="e4689-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="e4689-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4689-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4689-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4689-105">DESCRIPTION</span></span>
<span data-ttu-id="e4689-106">Этот командлет предназначен для использования в сценариях аварийного восстановления для проверки наличия полученного номера управления обменом и, при необходимости, для удаления этого объекта с помощью Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="e4689-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="e4689-107">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="e4689-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="e4689-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4689-108">EXAMPLES</span></span>

### <span data-ttu-id="e4689-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4689-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="e4689-110">Эта команда получает учетную запись интеграции X12, которая получила номер управляющего элемента управления обменом по названию соглашения и значению контрольного номера.</span><span class="sxs-lookup"><span data-stu-id="e4689-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="e4689-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e4689-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="e4689-112">Эта команда получает учетную запись интеграции EDIFACT, которая получила номер управляющего элемента управления обменом по названию соглашения и значению контрольного номера.</span><span class="sxs-lookup"><span data-stu-id="e4689-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="e4689-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4689-113">PARAMETERS</span></span>

### <span data-ttu-id="e4689-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="e4689-114">-AgreementName</span></span>
<span data-ttu-id="e4689-115">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e4689-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="e4689-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="e4689-116">-AgreementType</span></span>
<span data-ttu-id="e4689-117">Тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e4689-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="e4689-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="e4689-118">-ControlNumberValue</span></span>
<span data-ttu-id="e4689-119">Значение номера контроля учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e4689-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="e4689-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4689-120">-DefaultProfile</span></span>
<span data-ttu-id="e4689-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4689-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4689-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4689-122">-Name</span></span>
<span data-ttu-id="e4689-123">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e4689-123">The integration account name.</span></span>

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

### <span data-ttu-id="e4689-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4689-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4689-125">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e4689-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="e4689-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4689-126">CommonParameters</span></span>
<span data-ttu-id="e4689-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4689-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4689-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4689-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4689-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4689-129">INPUTS</span></span>

### <span data-ttu-id="e4689-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4689-130">System.String</span></span>

## <span data-ttu-id="e4689-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4689-131">OUTPUTS</span></span>

### <span data-ttu-id="e4689-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="e4689-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="e4689-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4689-133">NOTES</span></span>

## <span data-ttu-id="e4689-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4689-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4689-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="e4689-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="e4689-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="e4689-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
