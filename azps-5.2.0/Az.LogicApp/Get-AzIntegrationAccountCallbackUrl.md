---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409191"
---
# <span data-ttu-id="d500b-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d500b-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="d500b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d500b-102">SYNOPSIS</span></span>
<span data-ttu-id="d500b-103">Возвращает URL-адрес для интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="d500b-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="d500b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d500b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d500b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d500b-105">DESCRIPTION</span></span>
<span data-ttu-id="d500b-106">Cmdlet **Get-AzIntegrationAccountCallbackUrl получает URL-адрес** учетной записи для вызова интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d500b-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="d500b-107">Этот cmdlet возвращает объект **CallbackUrl,** который представляет URL-адрес обратного звонка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d500b-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="d500b-108">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d500b-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="d500b-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="d500b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d500b-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="d500b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d500b-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="d500b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d500b-112">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="d500b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d500b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d500b-113">EXAMPLES</span></span>

### <span data-ttu-id="d500b-114">Пример 1. Получите URL-адрес вызываемого звонка интеграции</span><span class="sxs-lookup"><span data-stu-id="d500b-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="d500b-115">Эта команда получает URL-адрес вызываемого звонка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d500b-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="d500b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d500b-116">PARAMETERS</span></span>

### <span data-ttu-id="d500b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d500b-117">-DefaultProfile</span></span>
<span data-ttu-id="d500b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d500b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d500b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d500b-119">-Name</span></span>
<span data-ttu-id="d500b-120">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d500b-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d500b-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="d500b-121">-NotAfter</span></span>
<span data-ttu-id="d500b-122">Указывает дату окончания срока действия URL-адреса для звонка.</span><span class="sxs-lookup"><span data-stu-id="d500b-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d500b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d500b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d500b-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d500b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d500b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d500b-125">CommonParameters</span></span>
<span data-ttu-id="d500b-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d500b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d500b-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d500b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d500b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d500b-128">INPUTS</span></span>

### <span data-ttu-id="d500b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d500b-129">System.String</span></span>

## <span data-ttu-id="d500b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d500b-130">OUTPUTS</span></span>

### <span data-ttu-id="d500b-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d500b-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="d500b-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d500b-132">NOTES</span></span>

## <span data-ttu-id="d500b-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d500b-133">RELATED LINKS</span></span>

[<span data-ttu-id="d500b-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="d500b-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


