---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 56e1ebdddd25b424a4fb59f2065831d2b54f21b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566986"
---
# <span data-ttu-id="b2bb6-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b2bb6-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="b2bb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bb6-103">Возвращает URL-адрес обратного вызова для учетной записи службы интеграции.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2bb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2bb6-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2bb6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="b2bb6-106">Командлет **Get-AzureRmIntegrationAccountCallbackUrl** возвращает URL-адрес обратной ссылки для учетной записи службы интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="b2bb6-107">Этот командлет возвращает объект **CallbackUrl** , представляющий URL-адрес обратной ссылки для учетной записи службы интеграции.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="b2bb6-108">Укажите имя учетной записи для интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="b2bb6-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b2bb6-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b2bb6-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b2bb6-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b2bb6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2bb6-113">EXAMPLES</span></span>

### <span data-ttu-id="b2bb6-114">Пример 1: получение URL-адреса обратной ссылки для учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="b2bb6-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="b2bb6-115">Эта команда возвращает URL-адрес обратного вызова для учетной записи службы интеграции.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="b2bb6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2bb6-116">PARAMETERS</span></span>

### <span data-ttu-id="b2bb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bb6-117">-DefaultProfile</span></span>
<span data-ttu-id="b2bb6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b2bb6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2bb6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2bb6-119">-Name</span></span>
<span data-ttu-id="b2bb6-120">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-120">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2bb6-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="b2bb6-121">-NotAfter</span></span>
<span data-ttu-id="b2bb6-122">Указывает дату истечения срока действия URL-адреса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bb6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2bb6-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2bb6-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b2bb6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bb6-125">CommonParameters</span></span>
<span data-ttu-id="b2bb6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bb6-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2bb6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bb6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2bb6-128">INPUTS</span></span>

### <span data-ttu-id="b2bb6-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="b2bb6-129">None</span></span>
<span data-ttu-id="b2bb6-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b2bb6-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2bb6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2bb6-131">OUTPUTS</span></span>

### <span data-ttu-id="b2bb6-132">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b2bb6-132">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="b2bb6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2bb6-133">NOTES</span></span>

## <span data-ttu-id="b2bb6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2bb6-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2bb6-135">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b2bb6-135">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


