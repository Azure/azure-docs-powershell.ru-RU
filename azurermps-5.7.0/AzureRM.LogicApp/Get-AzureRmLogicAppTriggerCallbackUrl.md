---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 7c7dcac142beb809b95c573d89ef0a912fd1d0b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560351"
---
# <span data-ttu-id="1f050-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1f050-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="1f050-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f050-102">SYNOPSIS</span></span>
<span data-ttu-id="1f050-103">Возвращает URL-адрес обратного вызова триггера приложения логики.</span><span class="sxs-lookup"><span data-stu-id="1f050-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f050-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f050-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f050-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f050-105">DESCRIPTION</span></span>
<span data-ttu-id="1f050-106">Командлет **Get-AzureRmLogicAppTriggerCallbackUrl** получает логическое приложение, вызывающее URL-адрес обратного вызова из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f050-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="1f050-107">Этот командлет возвращает объект **WorkflowTriggerCallbackUrl** , который представляет URL-адрес обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1f050-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="1f050-108">Укажите имя группы ресурсов, имя логического приложения и имя триггера.</span><span class="sxs-lookup"><span data-stu-id="1f050-108">Specify the resource group name, logic app name, and trigger name.</span></span>

<span data-ttu-id="1f050-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="1f050-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1f050-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="1f050-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1f050-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="1f050-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1f050-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="1f050-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1f050-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f050-113">EXAMPLES</span></span>

### <span data-ttu-id="1f050-114">Пример 1: получение URL-адреса обратного вызова триггера приложения логики</span><span class="sxs-lookup"><span data-stu-id="1f050-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="1f050-115">Эта команда возвращает URL-адрес обратного вызова триггера приложения логики.</span><span class="sxs-lookup"><span data-stu-id="1f050-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="1f050-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f050-116">PARAMETERS</span></span>

### <span data-ttu-id="1f050-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f050-117">-DefaultProfile</span></span>
<span data-ttu-id="1f050-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f050-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f050-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f050-119">-Name</span></span>
<span data-ttu-id="1f050-120">Указывает имя приложения логики.</span><span class="sxs-lookup"><span data-stu-id="1f050-120">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f050-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f050-121">-ResourceGroupName</span></span>
<span data-ttu-id="1f050-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f050-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1f050-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="1f050-123">-TriggerName</span></span>
<span data-ttu-id="1f050-124">Указывает имя триггера.</span><span class="sxs-lookup"><span data-stu-id="1f050-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="1f050-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f050-125">CommonParameters</span></span>
<span data-ttu-id="1f050-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f050-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f050-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f050-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f050-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f050-128">INPUTS</span></span>

### <span data-ttu-id="1f050-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="1f050-129">None</span></span>
<span data-ttu-id="1f050-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1f050-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f050-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f050-131">OUTPUTS</span></span>

### <span data-ttu-id="1f050-132">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1f050-132">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="1f050-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f050-133">NOTES</span></span>

## <span data-ttu-id="1f050-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f050-134">RELATED LINKS</span></span>

[<span data-ttu-id="1f050-135">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1f050-135">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)


