---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 434f59a7b81449fe0e07b0324c1df6408da1ce81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978920"
---
# <span data-ttu-id="3d765-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="3d765-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="3d765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d765-102">SYNOPSIS</span></span>
<span data-ttu-id="3d765-103">Содержит список ключа доступа для указанного магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d765-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="3d765-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d765-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d765-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d765-105">DESCRIPTION</span></span>
<span data-ttu-id="3d765-106">Содержит список ключа доступа для указанного магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d765-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="3d765-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d765-107">EXAMPLES</span></span>

### <span data-ttu-id="3d765-108">Пример 1. Список всех ключей магазина конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="3d765-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="3d765-109">В этой команде перечислены все ключи магазина конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="3d765-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="3d765-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d765-110">PARAMETERS</span></span>

### <span data-ttu-id="3d765-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d765-111">-DefaultProfile</span></span>
<span data-ttu-id="3d765-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d765-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d765-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3d765-113">-Name</span></span>
<span data-ttu-id="3d765-114">Имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3d765-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="3d765-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d765-115">-ResourceGroupName</span></span>
<span data-ttu-id="3d765-116">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="3d765-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="3d765-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d765-117">-SubscriptionId</span></span>
<span data-ttu-id="3d765-118">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d765-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d765-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d765-119">-Confirm</span></span>
<span data-ttu-id="3d765-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3d765-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d765-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d765-121">-WhatIf</span></span>
<span data-ttu-id="3d765-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d765-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d765-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3d765-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d765-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d765-124">CommonParameters</span></span>
<span data-ttu-id="3d765-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d765-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d765-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d765-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d765-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d765-127">INPUTS</span></span>

## <span data-ttu-id="3d765-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d765-128">OUTPUTS</span></span>

### <span data-ttu-id="3d765-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="3d765-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="3d765-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d765-130">NOTES</span></span>

<span data-ttu-id="3d765-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3d765-131">ALIASES</span></span>

## <span data-ttu-id="3d765-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d765-132">RELATED LINKS</span></span>

