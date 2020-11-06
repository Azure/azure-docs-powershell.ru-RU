---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561736"
---
# <span data-ttu-id="19a4b-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="19a4b-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="19a4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="19a4b-103">Возвращает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="19a4b-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19a4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19a4b-104">SYNTAX</span></span>

### <span data-ttu-id="19a4b-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19a4b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19a4b-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19a4b-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19a4b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19a4b-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19a4b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="19a4b-109">Командлет **Get-AzureRmLocationBasedServicesAccount** получает учетную запись службы на основе расположения в соответствии с группой ресурсов и именем либо идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="19a4b-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="19a4b-110">Кроме того, он может возвращать список всех учетных записей в ResourceGroup или все учетные записи служб на основе расположения для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="19a4b-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="19a4b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19a4b-111">EXAMPLES</span></span>

### <span data-ttu-id="19a4b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19a4b-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="19a4b-113">Возвращает учетную запись с именем Моя учетная запись в группе ресурсов MyResourceGroup, если она существует.</span><span class="sxs-lookup"><span data-stu-id="19a4b-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="19a4b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="19a4b-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="19a4b-115">Получает все учетные записи служб на основе расположения в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19a4b-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="19a4b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="19a4b-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="19a4b-117">Получает все учетные записи служб на основе расположения в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="19a4b-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="19a4b-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="19a4b-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="19a4b-119">Получает учетную запись служб на основе расположения, указанную идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="19a4b-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="19a4b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19a4b-120">PARAMETERS</span></span>

### <span data-ttu-id="19a4b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a4b-121">-DefaultProfile</span></span>
<span data-ttu-id="19a4b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19a4b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19a4b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19a4b-123">-Name</span></span>
<span data-ttu-id="19a4b-124">Имя учетной записи служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="19a4b-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a4b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19a4b-125">-ResourceGroupName</span></span>
<span data-ttu-id="19a4b-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19a4b-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a4b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19a4b-127">-ResourceId</span></span>
<span data-ttu-id="19a4b-128">ResourceId (учетная запись) служб на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="19a4b-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a4b-129">CommonParameters</span></span>
<span data-ttu-id="19a4b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19a4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a4b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19a4b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a4b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19a4b-132">INPUTS</span></span>

### <span data-ttu-id="19a4b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="19a4b-133">System.String</span></span>

## <span data-ttu-id="19a4b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19a4b-134">OUTPUTS</span></span>

### <span data-ttu-id="19a4b-135">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="19a4b-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="19a4b-136">Этот командлет возвращает объект **PSLocationBasedServicesAccount** .</span><span class="sxs-lookup"><span data-stu-id="19a4b-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="19a4b-137">Вы можете изменить этот объект, а затем применить изменения с помощью **Set-AzureRmLocationBasedServices**.</span><span class="sxs-lookup"><span data-stu-id="19a4b-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="19a4b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="19a4b-138">NOTES</span></span>

## <span data-ttu-id="19a4b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19a4b-139">RELATED LINKS</span></span>
