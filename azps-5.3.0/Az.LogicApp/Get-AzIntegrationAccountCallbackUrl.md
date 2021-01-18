---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518293"
---
# <span data-ttu-id="50322-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="50322-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="50322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50322-102">SYNOPSIS</span></span>
<span data-ttu-id="50322-103">Возвращает URL-адрес интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="50322-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="50322-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50322-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50322-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50322-105">DESCRIPTION</span></span>
<span data-ttu-id="50322-106">Cmdlet **Get-AzIntegrationAccountCallbackUrl получает URL-адрес** учетной записи для вызова интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50322-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="50322-107">Этот cmdlet возвращает объект **CallbackUrl,** который представляет URL-адрес обратного вызова учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="50322-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="50322-108">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50322-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="50322-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="50322-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="50322-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="50322-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="50322-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="50322-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="50322-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="50322-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="50322-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50322-113">EXAMPLES</span></span>

### <span data-ttu-id="50322-114">Пример 1. Получите URL-адрес вызываемого звонка интеграции</span><span class="sxs-lookup"><span data-stu-id="50322-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="50322-115">Эта команда получает URL-адрес вызываемого звонка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="50322-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="50322-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50322-116">PARAMETERS</span></span>

### <span data-ttu-id="50322-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50322-117">-DefaultProfile</span></span>
<span data-ttu-id="50322-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="50322-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50322-119">-Name</span><span class="sxs-lookup"><span data-stu-id="50322-119">-Name</span></span>
<span data-ttu-id="50322-120">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="50322-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="50322-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="50322-121">-NotAfter</span></span>
<span data-ttu-id="50322-122">Указывает дату окончания срока действия URL-адреса для звонка.</span><span class="sxs-lookup"><span data-stu-id="50322-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="50322-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50322-123">-ResourceGroupName</span></span>
<span data-ttu-id="50322-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50322-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="50322-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50322-125">CommonParameters</span></span>
<span data-ttu-id="50322-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50322-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50322-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50322-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50322-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50322-128">INPUTS</span></span>

### <span data-ttu-id="50322-129">System.String</span><span class="sxs-lookup"><span data-stu-id="50322-129">System.String</span></span>

## <span data-ttu-id="50322-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50322-130">OUTPUTS</span></span>

### <span data-ttu-id="50322-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="50322-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="50322-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50322-132">NOTES</span></span>

## <span data-ttu-id="50322-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50322-133">RELATED LINKS</span></span>

[<span data-ttu-id="50322-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="50322-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


