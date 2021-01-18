---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505845"
---
# <span data-ttu-id="8e841-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e841-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="8e841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e841-102">SYNOPSIS</span></span>
<span data-ttu-id="8e841-103">Получить свойство NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e841-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="8e841-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e841-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e841-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e841-105">DESCRIPTION</span></span>
<span data-ttu-id="8e841-106">Командлет **Get-AzStorageAccountNetworkRuleSet** получает свойство NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e841-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="8e841-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e841-107">EXAMPLES</span></span>

### <span data-ttu-id="8e841-108">Пример 1. Получить свойство NetworkRule указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e841-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="8e841-109">Эта команда получает свойство NetworkRule указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e841-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="8e841-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e841-110">PARAMETERS</span></span>

### <span data-ttu-id="8e841-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e841-111">-DefaultProfile</span></span>
<span data-ttu-id="8e841-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e841-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e841-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8e841-113">-Name</span></span>
<span data-ttu-id="8e841-114">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8e841-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e841-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e841-115">-ResourceGroupName</span></span>
<span data-ttu-id="8e841-116">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="8e841-116">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e841-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e841-117">CommonParameters</span></span>
<span data-ttu-id="8e841-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e841-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e841-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e841-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e841-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e841-120">INPUTS</span></span>

### <span data-ttu-id="8e841-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8e841-121">System.String</span></span>

## <span data-ttu-id="8e841-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e841-122">OUTPUTS</span></span>

### <span data-ttu-id="8e841-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e841-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="8e841-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e841-124">NOTES</span></span>

## <span data-ttu-id="8e841-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e841-125">RELATED LINKS</span></span>
