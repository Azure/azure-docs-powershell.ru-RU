---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7198e34e7e888c2e89fce6cb5293bfc46bf57b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968643"
---
# <span data-ttu-id="578ad-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="578ad-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="578ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578ad-102">SYNOPSIS</span></span>
<span data-ttu-id="578ad-103">Сведения о конфигурации Azure NetApp Files (ANF) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="578ad-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="578ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="578ad-104">SYNTAX</span></span>

### <span data-ttu-id="578ad-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="578ad-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="578ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="578ad-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="578ad-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="578ad-107">DESCRIPTION</span></span>
<span data-ttu-id="578ad-108">Для получения подробных сведений о конфигурации учетных записей ANF Active Directory можно получить сведения о **cmdlet Get-AzNetAppFilesActiveDirectory.**</span><span class="sxs-lookup"><span data-stu-id="578ad-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="578ad-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="578ad-109">EXAMPLES</span></span>

### <span data-ttu-id="578ad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="578ad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="578ad-111">Эта команда получает конфигурацию AD MyADConfigName для учетной записи Azure NetApp Files (ANF) с именем MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="578ad-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="578ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="578ad-112">PARAMETERS</span></span>

### <span data-ttu-id="578ad-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="578ad-113">-AccountName</span></span>
<span data-ttu-id="578ad-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="578ad-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="578ad-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="578ad-115">-AccountObject</span></span>
<span data-ttu-id="578ad-116">Учетная запись для нового объекта Active Directory</span><span class="sxs-lookup"><span data-stu-id="578ad-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="578ad-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="578ad-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="578ad-118">The ActiveDirectoryId of the ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="578ad-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="578ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578ad-119">-DefaultProfile</span></span>
<span data-ttu-id="578ad-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="578ad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="578ad-122">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="578ad-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="578ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578ad-123">CommonParameters</span></span>
<span data-ttu-id="578ad-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="578ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578ad-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="578ad-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578ad-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="578ad-126">INPUTS</span></span>

### <span data-ttu-id="578ad-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="578ad-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="578ad-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="578ad-128">OUTPUTS</span></span>

### <span data-ttu-id="578ad-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="578ad-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="578ad-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="578ad-130">NOTES</span></span>

## <span data-ttu-id="578ad-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="578ad-131">RELATED LINKS</span></span>
