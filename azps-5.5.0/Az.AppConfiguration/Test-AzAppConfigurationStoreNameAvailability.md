---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229396"
---
# <span data-ttu-id="d9764-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d9764-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="d9764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9764-102">SYNOPSIS</span></span>
<span data-ttu-id="d9764-103">Проверяет, доступно ли имя магазина конфигураций.</span><span class="sxs-lookup"><span data-stu-id="d9764-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="d9764-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d9764-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9764-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9764-105">DESCRIPTION</span></span>
<span data-ttu-id="d9764-106">Проверяет, доступно ли имя магазина конфигураций.</span><span class="sxs-lookup"><span data-stu-id="d9764-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="d9764-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d9764-107">EXAMPLES</span></span>

### <span data-ttu-id="d9764-108">Пример 1. Проверка доступности имени магазина конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="d9764-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="d9764-109">Эта команда проверяет доступность имени магазина конфигурации приложений.</span><span class="sxs-lookup"><span data-stu-id="d9764-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="d9764-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9764-110">PARAMETERS</span></span>

### <span data-ttu-id="d9764-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9764-111">-DefaultProfile</span></span>
<span data-ttu-id="d9764-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9764-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9764-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d9764-113">-Name</span></span>
<span data-ttu-id="d9764-114">Имя для проверки доступности.</span><span class="sxs-lookup"><span data-stu-id="d9764-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="d9764-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9764-115">-SubscriptionId</span></span>
<span data-ttu-id="d9764-116">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9764-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="d9764-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9764-117">-Confirm</span></span>
<span data-ttu-id="d9764-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9764-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9764-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9764-119">-WhatIf</span></span>
<span data-ttu-id="d9764-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9764-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9764-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d9764-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9764-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9764-122">CommonParameters</span></span>
<span data-ttu-id="d9764-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9764-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9764-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9764-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9764-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9764-125">INPUTS</span></span>

## <span data-ttu-id="d9764-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9764-126">OUTPUTS</span></span>

### <span data-ttu-id="d9764-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="d9764-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="d9764-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d9764-128">NOTES</span></span>

<span data-ttu-id="d9764-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d9764-129">ALIASES</span></span>

## <span data-ttu-id="d9764-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9764-130">RELATED LINKS</span></span>

