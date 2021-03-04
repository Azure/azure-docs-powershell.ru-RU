---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 03cb387b77dc2f003277b9f04a482f88a8da86fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958675"
---
# <span data-ttu-id="519d0-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="519d0-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="519d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="519d0-102">SYNOPSIS</span></span>
<span data-ttu-id="519d0-103">Получить ключи от учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="519d0-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="519d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="519d0-104">SYNTAX</span></span>

### <span data-ttu-id="519d0-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="519d0-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519d0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="519d0-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="519d0-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="519d0-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="519d0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="519d0-108">DESCRIPTION</span></span>
<span data-ttu-id="519d0-109">Получите ключи разработчика для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="519d0-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="519d0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="519d0-110">EXAMPLES</span></span>

### <span data-ttu-id="519d0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="519d0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="519d0-112">Получите ключи разработчика для удаленной отрисовки "example" из текущей подписки и группы ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="519d0-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="519d0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="519d0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="519d0-114">Получите ключи разработчика для удаленной отрисовки account "example" из текущей подписки и группы ресурсов "rg1" с piping.</span><span class="sxs-lookup"><span data-stu-id="519d0-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="519d0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="519d0-115">PARAMETERS</span></span>

### <span data-ttu-id="519d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519d0-116">-DefaultProfile</span></span>
<span data-ttu-id="519d0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="519d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="519d0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="519d0-118">-InputObject</span></span>
<span data-ttu-id="519d0-119">Объект пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="519d0-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="519d0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="519d0-120">-Name</span></span>
<span data-ttu-id="519d0-121">Имя учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="519d0-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="519d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="519d0-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="519d0-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519d0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="519d0-124">-ResourceId</span></span>
<span data-ttu-id="519d0-125">ИД ресурса учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="519d0-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519d0-126">CommonParameters</span></span>
<span data-ttu-id="519d0-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="519d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="519d0-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="519d0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519d0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="519d0-129">INPUTS</span></span>

### <span data-ttu-id="519d0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="519d0-130">System.String</span></span>

### <span data-ttu-id="519d0-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="519d0-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="519d0-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="519d0-132">OUTPUTS</span></span>

### <span data-ttu-id="519d0-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="519d0-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="519d0-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="519d0-134">NOTES</span></span>

## <span data-ttu-id="519d0-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="519d0-135">RELATED LINKS</span></span>
