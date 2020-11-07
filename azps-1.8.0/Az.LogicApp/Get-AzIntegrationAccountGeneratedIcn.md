---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 971e96b61b22bd5efbd22b82468d864a63392a16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899978"
---
# <span data-ttu-id="2da4b-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="2da4b-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="2da4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2da4b-102">SYNOPSIS</span></span>
<span data-ttu-id="2da4b-103">Этот командлет извлекает текущее значение сгенерированного номера элемента управления обменом для каждого соглашения.</span><span class="sxs-lookup"><span data-stu-id="2da4b-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="2da4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2da4b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2da4b-105">DESCRIPTION</span></span>
<span data-ttu-id="2da4b-106">Этот командлет предназначен для использования в сценариях аварийного восстановления, чтобы получить текущее значение сгенерированного номера элемента управления обменом, чтобы повторно записать увеличенное значение с помощью Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="2da4b-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="2da4b-107">Номер элемента управления различностью следует увеличить, чтобы избежать дублирования номеров управления обменом для номеров, которые еще не были реплицированы в пассивную область при аварии в активном регионе.</span><span class="sxs-lookup"><span data-stu-id="2da4b-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="2da4b-108">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="2da4b-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="2da4b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2da4b-109">EXAMPLES</span></span>

### <span data-ttu-id="2da4b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2da4b-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="2da4b-111">Эта команда используется для того, чтобы создать учетную запись для интеграции, созданную X12 управления ключами для наименования соглашения.</span><span class="sxs-lookup"><span data-stu-id="2da4b-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="2da4b-112">Убедитесь, что указанный контракт имеет тип "X12".</span><span class="sxs-lookup"><span data-stu-id="2da4b-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="2da4b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2da4b-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="2da4b-114">Эта команда используется для того, чтобы создать учетную запись для интеграции, созданную EDIFACT управления ключами для наименования соглашения.</span><span class="sxs-lookup"><span data-stu-id="2da4b-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="2da4b-115">Убедитесь, что указанный контракт имеет тип "EDIFACT".</span><span class="sxs-lookup"><span data-stu-id="2da4b-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="2da4b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2da4b-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="2da4b-117">Эта команда получает все созданные X12 элементы управления для обмена данными с именем учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2da4b-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="2da4b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2da4b-118">PARAMETERS</span></span>

### <span data-ttu-id="2da4b-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="2da4b-119">-AgreementName</span></span>
<span data-ttu-id="2da4b-120">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2da4b-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da4b-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="2da4b-121">-AgreementType</span></span>
<span data-ttu-id="2da4b-122">Тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2da4b-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="2da4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da4b-123">-DefaultProfile</span></span>
<span data-ttu-id="2da4b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2da4b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2da4b-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2da4b-125">-Name</span></span>
<span data-ttu-id="2da4b-126">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2da4b-126">The integration account name.</span></span>

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

### <span data-ttu-id="2da4b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da4b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2da4b-128">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="2da4b-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="2da4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da4b-129">CommonParameters</span></span>
<span data-ttu-id="2da4b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2da4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da4b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da4b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da4b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2da4b-132">INPUTS</span></span>

### <span data-ttu-id="2da4b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2da4b-133">System.String</span></span>

## <span data-ttu-id="2da4b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2da4b-134">OUTPUTS</span></span>

### <span data-ttu-id="2da4b-135">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="2da4b-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="2da4b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2da4b-136">NOTES</span></span>

## <span data-ttu-id="2da4b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2da4b-137">RELATED LINKS</span></span>

[<span data-ttu-id="2da4b-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="2da4b-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

