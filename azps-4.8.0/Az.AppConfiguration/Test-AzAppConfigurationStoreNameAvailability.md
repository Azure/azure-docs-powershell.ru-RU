---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077980"
---
# <span data-ttu-id="ac49a-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ac49a-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="ac49a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac49a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac49a-103">Проверяет, доступно ли имя хранилища конфигураций для использования.</span><span class="sxs-lookup"><span data-stu-id="ac49a-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ac49a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac49a-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac49a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac49a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac49a-106">Проверяет, доступно ли имя хранилища конфигураций для использования.</span><span class="sxs-lookup"><span data-stu-id="ac49a-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ac49a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac49a-107">EXAMPLES</span></span>

### <span data-ttu-id="ac49a-108">Пример 1: Проверка доступности имени хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="ac49a-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="ac49a-109">Эта команда проверяет доступность имени хранилища конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="ac49a-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="ac49a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac49a-110">PARAMETERS</span></span>

### <span data-ttu-id="ac49a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac49a-111">-DefaultProfile</span></span>
<span data-ttu-id="ac49a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac49a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac49a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac49a-113">-Name</span></span>
<span data-ttu-id="ac49a-114">Имя для проверки доступности.</span><span class="sxs-lookup"><span data-stu-id="ac49a-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="ac49a-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac49a-115">-SubscriptionId</span></span>
<span data-ttu-id="ac49a-116">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ac49a-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac49a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac49a-117">-Confirm</span></span>
<span data-ttu-id="ac49a-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac49a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac49a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac49a-119">-WhatIf</span></span>
<span data-ttu-id="ac49a-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac49a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac49a-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac49a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac49a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac49a-122">CommonParameters</span></span>
<span data-ttu-id="ac49a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac49a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac49a-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac49a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac49a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac49a-125">INPUTS</span></span>

## <span data-ttu-id="ac49a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac49a-126">OUTPUTS</span></span>

### <span data-ttu-id="ac49a-127">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ac49a-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="ac49a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac49a-128">NOTES</span></span>

<span data-ttu-id="ac49a-129">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ac49a-129">ALIASES</span></span>

## <span data-ttu-id="ac49a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac49a-130">RELATED LINKS</span></span>

