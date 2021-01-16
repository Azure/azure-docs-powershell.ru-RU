---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410815"
---
# <span data-ttu-id="5b304-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5b304-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="5b304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b304-102">SYNOPSIS</span></span>
<span data-ttu-id="5b304-103">Сведения о пуле файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="5b304-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="5b304-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b304-104">SYNTAX</span></span>

### <span data-ttu-id="5b304-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b304-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b304-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b304-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b304-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b304-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b304-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b304-108">DESCRIPTION</span></span>
<span data-ttu-id="5b304-109">Для получения сведений о пуле ANF можно получить подробные сведения о **cmdlet Get-AzNetAppFilesPool.**</span><span class="sxs-lookup"><span data-stu-id="5b304-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="5b304-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b304-110">EXAMPLES</span></span>

### <span data-ttu-id="5b304-111">Пример 1. Получить пул ANF</span><span class="sxs-lookup"><span data-stu-id="5b304-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="5b304-112">Эта команда получает учетную запись MyAnfPool из учетной записи MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="5b304-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="5b304-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b304-113">PARAMETERS</span></span>

### <span data-ttu-id="5b304-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b304-114">-AccountName</span></span>
<span data-ttu-id="5b304-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="5b304-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="5b304-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5b304-116">-AccountObject</span></span>
<span data-ttu-id="5b304-117">Объект учетной записи, содержащий пул, который нужно вернуть</span><span class="sxs-lookup"><span data-stu-id="5b304-117">The account object containing the pool to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b304-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b304-118">-DefaultProfile</span></span>
<span data-ttu-id="5b304-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b304-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b304-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b304-120">-Name</span></span>
<span data-ttu-id="5b304-121">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="5b304-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b304-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b304-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b304-123">Группа ресурсов пула ANF</span><span class="sxs-lookup"><span data-stu-id="5b304-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="5b304-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b304-124">-ResourceId</span></span>
<span data-ttu-id="5b304-125">ИД ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="5b304-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="5b304-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b304-126">CommonParameters</span></span>
<span data-ttu-id="5b304-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b304-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b304-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b304-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b304-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b304-129">INPUTS</span></span>

### <span data-ttu-id="5b304-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5b304-130">System.String</span></span>

### <span data-ttu-id="5b304-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5b304-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5b304-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b304-132">OUTPUTS</span></span>

### <span data-ttu-id="5b304-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5b304-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5b304-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b304-134">NOTES</span></span>

## <span data-ttu-id="5b304-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b304-135">RELATED LINKS</span></span>