---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313982"
---
# <span data-ttu-id="4a8a2-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4a8a2-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="4a8a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8a2-103">Получение состояния подписки для триггера событий для указанных внешних событий службы.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="4a8a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a8a2-104">SYNTAX</span></span>

### <span data-ttu-id="4a8a2-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a8a2-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a8a2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a8a2-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a8a2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a8a2-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a8a2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a8a2-108">DESCRIPTION</span></span>
<span data-ttu-id="4a8a2-109">Эта команда возвращает состояние подписки для триггера событий с указанными внешними событиями службы.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="4a8a2-110">Триггер не может быть запущен, пока не будет возвращено состояние "включено".</span><span class="sxs-lookup"><span data-stu-id="4a8a2-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="4a8a2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a8a2-111">EXAMPLES</span></span>

### <span data-ttu-id="4a8a2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a8a2-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="4a8a2-113">Эта команда получит состояние триггера subscribtion для BlobEnetTrigger1 внешних событий службы.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="4a8a2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a8a2-114">PARAMETERS</span></span>

### <span data-ttu-id="4a8a2-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4a8a2-115">-DataFactoryName</span></span>
<span data-ttu-id="4a8a2-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-116">The data factory name.</span></span>

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

### <span data-ttu-id="4a8a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8a2-117">-DefaultProfile</span></span>
<span data-ttu-id="4a8a2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a8a2-119">-InputObject</span></span>
<span data-ttu-id="4a8a2-120">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-120">The trigger object.</span></span>

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

### <span data-ttu-id="4a8a2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a8a2-121">-Name</span></span>
<span data-ttu-id="4a8a2-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-122">The trigger name.</span></span>

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

### <span data-ttu-id="4a8a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a8a2-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-124">The resource group name.</span></span>

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

### <span data-ttu-id="4a8a2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a8a2-125">-ResourceId</span></span>
<span data-ttu-id="4a8a2-126">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4a8a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8a2-127">CommonParameters</span></span>
<span data-ttu-id="4a8a2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8a2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a8a2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8a2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a8a2-130">INPUTS</span></span>

### <span data-ttu-id="4a8a2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4a8a2-131">System.String</span></span>
<span data-ttu-id="4a8a2-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="4a8a2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4a8a2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a8a2-133">OUTPUTS</span></span>

### <span data-ttu-id="4a8a2-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4a8a2-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="4a8a2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a8a2-135">NOTES</span></span>

## <span data-ttu-id="4a8a2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a8a2-136">RELATED LINKS</span></span>

