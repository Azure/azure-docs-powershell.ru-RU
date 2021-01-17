---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400908"
---
# <span data-ttu-id="40638-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="40638-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="40638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40638-102">SYNOPSIS</span></span>
<span data-ttu-id="40638-103">Войдите в реестр контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="40638-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="40638-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40638-104">SYNTAX</span></span>

### <span data-ttu-id="40638-105">WithoutNameAndPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40638-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40638-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="40638-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40638-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40638-107">DESCRIPTION</span></span>
<span data-ttu-id="40638-108">Войдите в реестр контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="40638-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="40638-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40638-109">EXAMPLES</span></span>

### <span data-ttu-id="40638-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40638-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="40638-111">Войдите в ACR без учетных данных, если вы уже входите в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="40638-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="40638-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40638-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="40638-113">Войдите в ACR с помощью имени пользователя и пароля администратора, когда была включена возможность администратора.</span><span class="sxs-lookup"><span data-stu-id="40638-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="40638-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="40638-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="40638-115">Войдите в ACR с помощью ИД основного приложения-службы и пароля.</span><span class="sxs-lookup"><span data-stu-id="40638-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="40638-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40638-116">PARAMETERS</span></span>

### <span data-ttu-id="40638-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40638-117">-DefaultProfile</span></span>
<span data-ttu-id="40638-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40638-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40638-119">-Name</span><span class="sxs-lookup"><span data-stu-id="40638-119">-Name</span></span>
<span data-ttu-id="40638-120">Имя реестра контейнера Azure.</span><span class="sxs-lookup"><span data-stu-id="40638-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40638-121">-Password</span><span class="sxs-lookup"><span data-stu-id="40638-121">-Password</span></span>
<span data-ttu-id="40638-122">Пароль для azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="40638-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40638-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="40638-123">-UserName</span></span>
<span data-ttu-id="40638-124">Имя пользователя для azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="40638-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40638-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40638-125">CommonParameters</span></span>
<span data-ttu-id="40638-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40638-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40638-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40638-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40638-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40638-128">INPUTS</span></span>

### <span data-ttu-id="40638-129">System.String</span><span class="sxs-lookup"><span data-stu-id="40638-129">System.String</span></span>

## <span data-ttu-id="40638-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40638-130">OUTPUTS</span></span>

### <span data-ttu-id="40638-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40638-131">System.Boolean</span></span>

## <span data-ttu-id="40638-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40638-132">NOTES</span></span>

## <span data-ttu-id="40638-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40638-133">RELATED LINKS</span></span>
