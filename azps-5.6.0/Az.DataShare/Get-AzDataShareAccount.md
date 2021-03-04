---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 7b47e54076441f1f4e78ec8cabc6a9dd3cd47153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954728"
---
# <span data-ttu-id="8e466-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="8e466-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="8e466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e466-102">SYNOPSIS</span></span>
<span data-ttu-id="8e466-103">Сведения об учетных записях DataShare</span><span class="sxs-lookup"><span data-stu-id="8e466-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="8e466-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e466-104">SYNTAX</span></span>

### <span data-ttu-id="8e466-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e466-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e466-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e466-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e466-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e466-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e466-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e466-108">DESCRIPTION</span></span>
<span data-ttu-id="8e466-109">Для получения сведений об учетных записях datashare в группе подписок и ресурсов Azure можно получить сведения об учетных записях **Get-AzDataShareAccount.**</span><span class="sxs-lookup"><span data-stu-id="8e466-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="8e466-110">Если указать имя учетной записи, этот cmdlet получит сведения об этой учетной записи datshare.</span><span class="sxs-lookup"><span data-stu-id="8e466-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="8e466-111">Если имя не указано, этот cmdlet получает сведения обо всех учетных записях datashare в группе подписок и ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8e466-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="8e466-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e466-112">EXAMPLES</span></span>

### <span data-ttu-id="8e466-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e466-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="8e466-114">Эта команда отображает сведения обо всех учетных записях datashare в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="8e466-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="8e466-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e466-115">PARAMETERS</span></span>

### <span data-ttu-id="8e466-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e466-116">-DefaultProfile</span></span>
<span data-ttu-id="8e466-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e466-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e466-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8e466-118">-Name</span></span>
<span data-ttu-id="8e466-119">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="8e466-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e466-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e466-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e466-121">Имя группы ресурсов учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="8e466-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e466-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e466-122">-ResourceId</span></span>
<span data-ttu-id="8e466-123">ИД ресурса учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="8e466-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e466-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e466-124">CommonParameters</span></span>
<span data-ttu-id="8e466-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e466-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e466-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e466-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e466-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e466-127">INPUTS</span></span>

### <span data-ttu-id="8e466-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8e466-128">System.String</span></span>

## <span data-ttu-id="8e466-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e466-129">OUTPUTS</span></span>

### <span data-ttu-id="8e466-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="8e466-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="8e466-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e466-131">NOTES</span></span>

## <span data-ttu-id="8e466-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e466-132">RELATED LINKS</span></span>
