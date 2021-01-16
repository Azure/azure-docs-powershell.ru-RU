---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410855"
---
# <span data-ttu-id="3aed4-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3aed4-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="3aed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aed4-102">SYNOPSIS</span></span>
<span data-ttu-id="3aed4-103">Сведения об учетной записи Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="3aed4-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="3aed4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3aed4-104">SYNTAX</span></span>

### <span data-ttu-id="3aed4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3aed4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aed4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aed4-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aed4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aed4-107">DESCRIPTION</span></span>
<span data-ttu-id="3aed4-108">Для получения сведений об учетной записи ANF возвращается **cmdlet Get-AzNetAppFilesAccount.**</span><span class="sxs-lookup"><span data-stu-id="3aed4-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="3aed4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3aed4-109">EXAMPLES</span></span>

### <span data-ttu-id="3aed4-110">Пример 1. Получить учетную запись ANF</span><span class="sxs-lookup"><span data-stu-id="3aed4-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="3aed4-111">Эта команда получает учетную запись с именем MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="3aed4-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="3aed4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aed4-112">PARAMETERS</span></span>

### <span data-ttu-id="3aed4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aed4-113">-DefaultProfile</span></span>
<span data-ttu-id="3aed4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3aed4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aed4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3aed4-115">-Name</span></span>
<span data-ttu-id="3aed4-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="3aed4-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aed4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aed4-117">-ResourceGroupName</span></span>
<span data-ttu-id="3aed4-118">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="3aed4-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aed4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aed4-119">-ResourceId</span></span>
<span data-ttu-id="3aed4-120">ИД ресурса учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="3aed4-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="3aed4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aed4-121">CommonParameters</span></span>
<span data-ttu-id="3aed4-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aed4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aed4-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aed4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aed4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3aed4-124">INPUTS</span></span>

### <span data-ttu-id="3aed4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3aed4-125">System.String</span></span>

## <span data-ttu-id="3aed4-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3aed4-126">OUTPUTS</span></span>

### <span data-ttu-id="3aed4-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3aed4-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="3aed4-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3aed4-128">NOTES</span></span>

## <span data-ttu-id="3aed4-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aed4-129">RELATED LINKS</span></span>
