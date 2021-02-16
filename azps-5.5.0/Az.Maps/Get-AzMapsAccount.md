---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226321"
---
# <span data-ttu-id="26acb-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="26acb-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="26acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26acb-102">SYNOPSIS</span></span>
<span data-ttu-id="26acb-103">Получает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="26acb-103">Gets the account.</span></span>

## <span data-ttu-id="26acb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26acb-104">SYNTAX</span></span>

### <span data-ttu-id="26acb-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26acb-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26acb-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26acb-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26acb-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26acb-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26acb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26acb-108">DESCRIPTION</span></span>
<span data-ttu-id="26acb-109">Этот Get-AzMapsAccount получает резервную учетную запись Azure Maps по группе ресурсов и имени либо по коду ресурса. Кроме того, она может вернуть список всех учетных записей в группе ресурсов или всех учетных записей Azure Maps для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="26acb-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="26acb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26acb-110">EXAMPLES</span></span>

### <span data-ttu-id="26acb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26acb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="26acb-112">Возвращает учетную запись MyAccount в группе ресурсов MyResourceGroup, если она существует.</span><span class="sxs-lookup"><span data-stu-id="26acb-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="26acb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="26acb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="26acb-114">Получает все учетные записи Azure Maps в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="26acb-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="26acb-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="26acb-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="26acb-116">Получает все учетные записи Azure Maps в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="26acb-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="26acb-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="26acb-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="26acb-118">Возвращает учетную запись "Карты", указанную в ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="26acb-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="26acb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26acb-119">PARAMETERS</span></span>

### <span data-ttu-id="26acb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26acb-120">-DefaultProfile</span></span>
<span data-ttu-id="26acb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26acb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26acb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="26acb-122">-Name</span></span>
<span data-ttu-id="26acb-123">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="26acb-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26acb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26acb-124">-ResourceGroupName</span></span>
<span data-ttu-id="26acb-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26acb-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26acb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26acb-126">-ResourceId</span></span>
<span data-ttu-id="26acb-127">Карты Account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="26acb-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26acb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26acb-128">CommonParameters</span></span>
<span data-ttu-id="26acb-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26acb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26acb-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26acb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26acb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26acb-131">INPUTS</span></span>

### <span data-ttu-id="26acb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="26acb-132">System.String</span></span>

## <span data-ttu-id="26acb-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26acb-133">OUTPUTS</span></span>

### <span data-ttu-id="26acb-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="26acb-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="26acb-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26acb-135">NOTES</span></span>

## <span data-ttu-id="26acb-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26acb-136">RELATED LINKS</span></span>
