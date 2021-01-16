---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400812"
---
# <span data-ttu-id="43364-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="43364-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="43364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43364-102">SYNOPSIS</span></span>
<span data-ttu-id="43364-103">Создание учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="43364-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="43364-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43364-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43364-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43364-105">DESCRIPTION</span></span>
<span data-ttu-id="43364-106">Создайте новую учетную запись удаленной отрисовки в определенной подписке, группе ресурсов и регионе.</span><span class="sxs-lookup"><span data-stu-id="43364-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="43364-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43364-107">EXAMPLES</span></span>

### <span data-ttu-id="43364-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43364-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="43364-109">Создайте новый "пример" учетной записи удаленной отрисовки в текущей подписке, группе ресурсов "rg1" и Центре США.</span><span class="sxs-lookup"><span data-stu-id="43364-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="43364-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43364-110">PARAMETERS</span></span>

### <span data-ttu-id="43364-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43364-111">-Confirm</span></span>
<span data-ttu-id="43364-112">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43364-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43364-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43364-113">-DefaultProfile</span></span>
<span data-ttu-id="43364-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43364-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43364-115">-Location</span><span class="sxs-lookup"><span data-stu-id="43364-115">-Location</span></span>
<span data-ttu-id="43364-116">Расположение учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="43364-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43364-117">-Name</span><span class="sxs-lookup"><span data-stu-id="43364-117">-Name</span></span>
<span data-ttu-id="43364-118">Имя учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="43364-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43364-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43364-119">-ResourceGroupName</span></span>
<span data-ttu-id="43364-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43364-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43364-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43364-121">-WhatIf</span></span>
<span data-ttu-id="43364-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43364-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43364-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43364-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43364-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43364-124">CommonParameters</span></span>
<span data-ttu-id="43364-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43364-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="43364-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43364-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43364-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43364-127">INPUTS</span></span>

### <span data-ttu-id="43364-128">Нет</span><span class="sxs-lookup"><span data-stu-id="43364-128">None</span></span>

## <span data-ttu-id="43364-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43364-129">OUTPUTS</span></span>

### <span data-ttu-id="43364-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="43364-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="43364-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43364-131">NOTES</span></span>

## <span data-ttu-id="43364-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43364-132">RELATED LINKS</span></span>