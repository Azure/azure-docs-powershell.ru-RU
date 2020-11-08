---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079020"
---
# <span data-ttu-id="28dc0-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="28dc0-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="28dc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="28dc0-103">Возвращает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="28dc0-103">Gets the account.</span></span>

## <span data-ttu-id="28dc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28dc0-104">SYNTAX</span></span>

### <span data-ttu-id="28dc0-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28dc0-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28dc0-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dc0-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28dc0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dc0-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28dc0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28dc0-108">DESCRIPTION</span></span>
<span data-ttu-id="28dc0-109">Командлет Get-AzMapsAccount возвращает подготовленную учетную запись карт Azure: по группе ресурсов и имени или по идентификатору ресурса. Кроме того, он может возвращать список всех учетных записей в группе ResourceGroup или все учетные записи карт Azure для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="28dc0-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="28dc0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28dc0-110">EXAMPLES</span></span>

### <span data-ttu-id="28dc0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28dc0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="28dc0-112">Возвращает учетную запись с именем Моя учетная запись в группе ресурсов MyResourceGroup, если она существует.</span><span class="sxs-lookup"><span data-stu-id="28dc0-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="28dc0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="28dc0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="28dc0-114">Получает все учетные записи карт Azure в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="28dc0-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="28dc0-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="28dc0-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="28dc0-116">Получает все учетные записи карт Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="28dc0-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="28dc0-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="28dc0-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="28dc0-118">Получает учетную запись карт, заданную идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="28dc0-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="28dc0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28dc0-119">PARAMETERS</span></span>

### <span data-ttu-id="28dc0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28dc0-120">-DefaultProfile</span></span>
<span data-ttu-id="28dc0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28dc0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28dc0-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28dc0-122">-Name</span></span>
<span data-ttu-id="28dc0-123">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="28dc0-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="28dc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28dc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="28dc0-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28dc0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="28dc0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28dc0-126">-ResourceId</span></span>
<span data-ttu-id="28dc0-127">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="28dc0-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="28dc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28dc0-128">CommonParameters</span></span>
<span data-ttu-id="28dc0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28dc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28dc0-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28dc0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28dc0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28dc0-131">INPUTS</span></span>

### <span data-ttu-id="28dc0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="28dc0-132">System.String</span></span>

## <span data-ttu-id="28dc0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28dc0-133">OUTPUTS</span></span>

### <span data-ttu-id="28dc0-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="28dc0-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="28dc0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="28dc0-135">NOTES</span></span>

## <span data-ttu-id="28dc0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28dc0-136">RELATED LINKS</span></span>
