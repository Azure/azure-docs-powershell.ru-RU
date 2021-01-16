---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412564"
---
# <span data-ttu-id="59185-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="59185-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="59185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59185-102">SYNOPSIS</span></span>
<span data-ttu-id="59185-103">Получите состояние подписки для триггера события для указанных событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="59185-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="59185-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59185-104">SYNTAX</span></span>

### <span data-ttu-id="59185-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59185-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59185-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59185-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59185-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59185-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59185-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59185-108">DESCRIPTION</span></span>
<span data-ttu-id="59185-109">Эта команда получает состояние подписки на триггер события для указанных событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="59185-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="59185-110">Триггер нельзя запускать, пока не будет возвращено состояние "Включено".</span><span class="sxs-lookup"><span data-stu-id="59185-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="59185-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59185-111">EXAMPLES</span></span>

### <span data-ttu-id="59185-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59185-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="59185-113">Эта команда будет получать состояние подписки на триггер BlobEnetTrigger1 для событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="59185-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="59185-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59185-114">PARAMETERS</span></span>

### <span data-ttu-id="59185-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="59185-115">-DataFactoryName</span></span>
<span data-ttu-id="59185-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="59185-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59185-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59185-117">-DefaultProfile</span></span>
<span data-ttu-id="59185-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59185-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59185-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59185-119">-InputObject</span></span>
<span data-ttu-id="59185-120">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="59185-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59185-121">-Name</span><span class="sxs-lookup"><span data-stu-id="59185-121">-Name</span></span>
<span data-ttu-id="59185-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="59185-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59185-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59185-123">-ResourceGroupName</span></span>
<span data-ttu-id="59185-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59185-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59185-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59185-125">-ResourceId</span></span>
<span data-ttu-id="59185-126">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="59185-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59185-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59185-127">CommonParameters</span></span>
<span data-ttu-id="59185-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59185-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59185-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59185-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59185-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59185-130">INPUTS</span></span>

### <span data-ttu-id="59185-131">System.String</span><span class="sxs-lookup"><span data-stu-id="59185-131">System.String</span></span>
<span data-ttu-id="59185-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="59185-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="59185-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59185-133">OUTPUTS</span></span>

### <span data-ttu-id="59185-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="59185-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="59185-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59185-135">NOTES</span></span>

## <span data-ttu-id="59185-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59185-136">RELATED LINKS</span></span>
